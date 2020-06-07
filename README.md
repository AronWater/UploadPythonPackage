UploadPythonPackage 
======================
This is a simple repo showing you how to upload a package to python




Step
==============================================

1. Clone this repository
2. Look at the setup.py to see what you wanna change, you would like to have a different package name
3. Install `setuptools` and `wheel3`

`python3 -m pip install --user --upgrade setuptools wheel`

4. python3 setup.py sdist bdist_wheel
5. Install Twine 

`python3 -m pip install --user --upgrade twine`

6. Register an account in  https://test.pypi.org/account/register/

7. Run Twine

`python3 -m twine upload --repository testpypi dist/*`

8. Input your username and password

`Uploading distributions to https://test.pypi.org/legacy/
Enter your username: [your username]        ##########  HERE IS YOUR  USERNAME
Enter your password:                        ##########  HERE IS YOUR  PASSWORD
Uploading example_pkg_YOUR_USERNAME_HERE-0.0.1-py3-none-any.whl
100%|█████████████████████| 4.65k/4.65k [00:01<00:00, 2.88kB/s]
Uploading example_pkg_YOUR_USERNAME_HERE-0.0.1.tar.gz
100%|█████████████████████| 4.25k/4.25k [00:01<00:00, 3.05kB/s]`

9. View your uploaded project in  https://test.pypi.org/project/example-pkg-YOUR-USERNAME-HERE
