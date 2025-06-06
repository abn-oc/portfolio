<script lang="ts" context="module">
  export function copyClipboard(msg: string, duration: number = 2000) {
  const textArea = document.createElement("textarea");
  textArea.value = msg;
  // Prevent scrolling to bottom
  textArea.style.position = "fixed";
  textArea.style.top = "0";
  textArea.style.left = "0";
  textArea.style.width = "2em";
  textArea.style.height = "2em";
  textArea.style.padding = "0";
  textArea.style.border = "none";
  textArea.style.outline = "none";
  textArea.style.boxShadow = "none";
  textArea.style.background = "transparent";

  document.body.appendChild(textArea);
  textArea.focus();
  textArea.select();

  let successful = false;
  try {
    successful = document.execCommand('copy');
  } catch {
    successful = false;
  }

  document.body.removeChild(textArea);

  if (successful) {
    const toast = document.createElement('div');
    toast.textContent = "Copied to Clipboard!";
    Object.assign(toast.style, {
      position: 'fixed',
      top: '1rem',
      right: '1rem',
      background: 'black',
      color: 'white',
      padding: '0.5rem 1rem',
      borderRadius: '4px',
      fontSize: '14px',
      opacity: '1',
      transition: 'opacity 0.5s',
      zIndex: 9999,
    });
    document.body.appendChild(toast);
    setTimeout(() => {
      toast.style.opacity = '0';
      toast.addEventListener('transitionend', () => toast.remove());
    }, duration);
  } else {
    alert("Failed to copy text.");
  }
}

</script>
