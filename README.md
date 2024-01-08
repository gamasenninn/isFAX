# Audio FAX Detector

This Python script allows you to detect whether an audio file contains FAX-like characteristics by analyzing its frequency components. FAX audio signals typically exhibit specific frequency ranges, and this script checks if those frequencies are present in the given audio file.

## Usage

1. Install the required libraries:

   ```
   pip install pydub numpy
   ```

2. Run the script with the path to your audio file as an argument:

   ```
   python isfax.py <audio_file_path>
   ```

   Replace `<audio_file_path>` with the path to your audio file in the M4A format.

## Description

The script performs the following steps:

1. Loads the audio file, normalizes the audio data, and calculates its FFT (Fast Fourier Transform) to obtain frequency and amplitude information.

2. Identifies the top frequencies based on their amplitudes.

3. Checks if the specified target frequency ranges associated with FAX signals are present in the audio data.

4. Provides feedback on whether the target frequency ranges are found in the audio file, indicating whether it exhibits FAX-like characteristics.

## Target Frequency Ranges

The script checks for the presence of the following target frequency ranges, which are typically associated with FAX signals:

- 1660 Hz to 1665 Hz
- 2099 Hz to 2100 Hz

## Output

The script will output whether the specified target frequency ranges are found in the audio file. If found, it will indicate that the frequency ranges associated with FAX signals exist in the audio.

## Example

```bash
python isfax.py path_to_audio_file.m4a
```

The script will provide feedback on the presence of FAX-like characteristics in the specified audio file.

## License

This script is open-source and available under the [MIT License](LICENSE).
