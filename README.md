# RePaint--no-resample
This code disables repaint resampling method and use mean of batch to get inpainting

The source code I used in:
https://github.com/andreas128/RePaint

the main changes I made are:
1. Changed number of resamples and jump lenght to 1 to avoide resampling (in conf file and guided_figgusion.scheduler).
2. Added a batch size - so the same image sampled for batch_size times.
3. Saved the mean of the result (on batch_size dim).
4. Used a for loop to take the mean of (result_befor,result) - instead of using large batch_size.
