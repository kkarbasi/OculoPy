# OculoPy: Python package for saccade detection

## System requirements:
This code has been tested on Python 3. Required packages can be found in [requirements.txt](https://github.com/kkarbasi/OculoPy/blob/master/requirements.txt)

## Usage

Assuming horizonal eye trace is in eye_x and vertical eye_trace is in eye_y:

- _Fs_: sampling frequency
- _eye_x_t_: horizontal eye trace timestamps 
- _eye_y_t_: vertical eye trace timestamps

`from OculoPy import SaccadeDetector`

`new_session = SaccadeDetector(HE = eye_x, t_HE = eye_x_t, VE = eye_y, t_VE = eye_y_t, eye_fs = Fs)`

`new_session._calc_saccade_velocity()`

`new_session._detect_saccades()`

After a successful run the indices for detected saccades can be accessed through following class variables:
* __new_session.saccade_onsets:__ saccade onset indices
* __new_session.saccade_offsets:__ saccade offset indices

* __new_session.saccade_onset_times:__ saccade onset times
* __new_session.saccade_offset_times:__ saccade offset times


 

