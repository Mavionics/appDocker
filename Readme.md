# Readme

## Build image

```
sudo docker build -t owodunni/mavionics-android .
```
## Use image

Make sure android folder dosn't contain a properties.local file. If it does gradle can not find the SDK.

```
sudo docker run -it --rm -v $PWD:/root/tmp mavionics:android-build  bash
```

Now you can build the mavionics app as you would without the docker image

## Deploy image

```
sudo docker login --username=owodunni
```
```
sudo docker tag a9fc84119b78 owodunni/mavionics-android:0.1.0
```
```
sudo docker push owodunni/mavionics-android:0.1.0
```