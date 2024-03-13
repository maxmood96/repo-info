## `mongo:5-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:0626200f3b9919a94b797a04f72f5063ebd725e25af0c74f65db2357c6963983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `mongo:5-nanoserver-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull mongo@sha256:24f5581ec34379ff3bf9488c1d4147554770def151e72a5cac8ea3dac17c118b
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.1 MB (436060361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c49056cabec1fc224105a0c94c950116d78ba0d5348af1092545dc2889e670`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 05 Mar 2024 19:20:30 GMT
RUN Apply image 10.0.20348.2340
# Wed, 13 Mar 2024 02:03:29 GMT
SHELL [cmd /S /C]
# Wed, 13 Mar 2024 02:03:30 GMT
USER ContainerAdministrator
# Wed, 13 Mar 2024 02:03:33 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 13 Mar 2024 02:03:33 GMT
USER ContainerUser
# Wed, 13 Mar 2024 02:03:35 GMT
COPY multi:c5f0fbe231f542d852dcd0a8e1790eb7694672a9238df11d11d4dd7ca117b6a8 in C:\Windows\System32\ 
# Wed, 13 Mar 2024 02:03:36 GMT
ENV MONGO_VERSION=5.0.25
# Wed, 13 Mar 2024 02:03:50 GMT
COPY dir:95d30a603d2e71c517181ebf96eae248a855a0fc4e8e1503c7f181fcfaf159de in C:\mongodb 
# Wed, 13 Mar 2024 02:04:01 GMT
RUN mongo --version && mongod --version
# Wed, 13 Mar 2024 02:04:01 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 13 Mar 2024 02:04:02 GMT
EXPOSE 27017
# Wed, 13 Mar 2024 02:04:03 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:94ec3b200bababb5c0b6605ad82c23779d8f918fbfe1ef5d1cf51be6f12fa749`  
		Last Modified: Tue, 12 Mar 2024 19:42:37 GMT  
		Size: 120.7 MB (120702694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7182bf08e60c6990f2280955e1bba513503c792aec9550a265e5761781431168`  
		Last Modified: Wed, 13 Mar 2024 02:04:11 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053872a5839bbdc35dba6160cbd25295a688893257e2263c4c82fc2e939c6261`  
		Last Modified: Wed, 13 Mar 2024 02:04:11 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d491029f2194aa53d8ef9002da4f4524473f8ece87c3bbf166074cffa878f99`  
		Last Modified: Wed, 13 Mar 2024 02:04:09 GMT  
		Size: 78.8 KB (78774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274ed12598d34beb28b9c82e7ee42d336dfb02f8b27aaa5e599adfbc81e6ddbe`  
		Last Modified: Wed, 13 Mar 2024 02:04:09 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea371648791eff2edfbcde67d325b93c5f69475874a799ed6b30d4bf60f070ac`  
		Last Modified: Wed, 13 Mar 2024 02:04:09 GMT  
		Size: 267.4 KB (267437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a51efdf667edba793bfe8f7524936d822972af992bbb974e304eec0cfd57f6`  
		Last Modified: Wed, 13 Mar 2024 02:04:09 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79a89fcc8e22a1539a02cbd486d2aa93329fa3565598db4f397b3ae5ab150353`  
		Last Modified: Wed, 13 Mar 2024 02:04:38 GMT  
		Size: 314.9 MB (314913628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bd239e66586d68e08fc4e28cf1b7c4b9319b6417634adeb7cf56bf1435c987f`  
		Last Modified: Wed, 13 Mar 2024 02:04:07 GMT  
		Size: 90.5 KB (90545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fdd605bd1a757ece6d768731a288d704d15698b1aed0b1444f90eb51694d4e`  
		Last Modified: Wed, 13 Mar 2024 02:04:07 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9307e66cd5dc169d7e6c65412fabaad3a81baa590e2e0dd63619bfe834d410f6`  
		Last Modified: Wed, 13 Mar 2024 02:04:07 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8327d4429b9bce4ad4d94f8e2039eb73c969d3ac489ddf5c9cc9bdcf8e2f9d8f`  
		Last Modified: Wed, 13 Mar 2024 02:04:07 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
