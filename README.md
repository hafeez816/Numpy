
 1. numpy.loadtxt() – For reading text files
python
Copy
Edit
import numpy as np

data = np.loadtxt('filename.txt', delimiter=',')  # use delimiter if needed
print(data)
Parameters:

'filename.txt' – Path to your file

delimiter=',' – (Optional) Use this if the file is CSV or other delimited text

 2. numpy.genfromtxt() – Like loadtxt, but handles missing data better
python
Copy
Edit
import numpy as np

data = np.genfromtxt('filename.txt', delimiter=',', skip_header=1)
print(data)
 3. numpy.load() – For reading .npy binary files (NumPy's native format)
python
Copy
Edit
import numpy as np

data = np.load('filename.npy')
print(data)
 4. numpy.load() (with allow_pickle=True) – For .npz files (compressed archive)
python
Copy
Edit
import numpy as np

data = np.load('filename.npz', allow_pickle=True)

for key in data:
    print(f"{key}: {data[key]}")
Example Text File: data.txt
Copy
Edit
1.0, 2.0, 3.0
4.0, 5.0, 6.0
7.0, 8.0, 9.0
Reading it:

python
Copy
Edit
import numpy as np

data = np.loadtxt('data.txt', delimiter=',')
print(data)
