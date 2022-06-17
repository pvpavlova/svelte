<script>
    export let color;
    export let colorType;
  </script>
  
  <div>
      <label for={`${colorType}-input`}>{colorType} - {color}</label>
      <input id={`${colorType}-input`} type="range"
     min="0" max="255" bind:value={color}
    />
  </div>
  <style>
    input,
    label {
      display: block;
      margin: 10px;
    }
    input {
      width: 80%;
    }
    label {
      font-size: 24px;
    }
  </style>