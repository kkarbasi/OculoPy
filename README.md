OculoPy: Python package for saccade detection

## System requirements:
This code has been tested on Python 3. Required packages can be found in [requirements.txt](https://github.com/kkarbasi/OculoPy/blob/master/requirements.txt)

## Usage

Assuming horizonal eye trace is in eye_x and vertical eye_trace is in eye_y:
Fs: sampling frequency
eye_x_t: horizontal eye trace timestamps 
eye_y_t: vertical eye trace timestamps

`from OculoPy import SaccadeDetector`

`new_session = SaccadeDetector(HE = eye_x, t_HE = eye_x_t, VE = eye_y, t_VE = eye_y_t, eye_fs = Fs)
`new_session.run()`

After a successful run the indices for detected saccades can be accessed through following class variables:
new_session.saccade_onsets: saccade onset indices
new_session.saccade_offsets: saccade offset indices

new_session.saccade_onset_times: saccade onset times
new_session.saccade_offset_times: saccade offset times


 

