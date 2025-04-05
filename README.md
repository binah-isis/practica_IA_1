<button id="copyButton" style="margin-top: 10px; padding: 10px; background-color: #007bff; color: white; border: none; border-radius: 5px; cursor: pointer;">Copiar al Portapapeles</button>
      `,
      showConfirmButton: false,
      didOpen: () => {
        // Agregar funcionalidad para copiar al portapapeles
        const copyButton = document.getElementById('copyButton');
        copyButton.addEventListener('click', () => {
          const textarea = document.querySelector('.swal2-html-container textarea');
          textarea.select();
          document.execCommand('copy');
          Swal.fire({
            icon: 'success',
            title: 'Copiado',
            text: 'El código ha sido copiado al portapapeles.',
            timer: 1500,
            showConfirmButton: false,
          });
        });
      }
    });
  }
});
