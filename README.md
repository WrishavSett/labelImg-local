1. Open Terminal
2. Make a new directory named `labelImg`
3. Make a new virtual environment named `.venv`
4. Activate the virtual environment
5. Install the following packages:
    ```
    pip install pyqt5 lxml
    ```
6. Clone the LabelImg repository from:
   > https://github.com/HumanSignal/labelImg.git
7. Navigate to the `labelImg` directory
8. Execute the following command:
   ```
   pyrcc5 -o libs/resources.py resources.qrc
   ```
9.  Now run LabelImg tool:
    ```
    python labelImg.py
    ```
10. To make an installer:
    ```
    pip install pyinstaller
    pyinstaller --hidden-import=pyqt5 --hidden-import=lxml -F -n "labelImg" -c labelImg.py -p ./libs -p ./
    ```
11. Find the installer at:
    > labelImg\labelImg\dist