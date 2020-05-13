## `nats-streaming:windowsservercore`

```console
$ docker pull nats-streaming@sha256:b8a405d0a1d1f76c1d87fe602914f99e1c50ab461a77bd64742b4632cefaba81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3686; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.14393.3686; amd64

```console
$ docker pull nats-streaming@sha256:d7bc076f9afe08fb7abcff9a3d924e3189fb6a63cb04e394f5b6fa81170de88c
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5737947000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6449a3e6f97d73e9293f5326232c102813ed07bf6914be0e5837a2b783eab610`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 18:55:40 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 May 2020 18:55:42 GMT
RUN cmd /S /C #(nop) WORKDIR C:\nats-streaming-server
# Wed, 13 May 2020 18:55:43 GMT
RUN cmd /S /C #(nop) COPY file:d30725f7225d14fba35e88513adf63da18fc9fef9c4f6c817dff8f784f19a7c1 in nats-streaming-server.exe 
# Wed, 13 May 2020 18:55:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 13 May 2020 18:55:46 GMT
RUN cmd /S /C #(nop)  CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b940e70a4619b357d89f3dcabf4ac263d1efc65e1ef3af64cb0e8fbeaccc64dd`  
		Size: 1.7 GB (1661903967 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4fd341c753cc109806184352c1ee6cd56190748bda7c96f8c4bf684501c4a103`  
		Last Modified: Wed, 13 May 2020 18:57:15 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b052abee2d10114a0a2f59ac34b6c8e5e39560792ca3ea1c6febe9647c0f1cd0`  
		Last Modified: Wed, 13 May 2020 18:57:15 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d106a96d9a17da18ea6867e053d6772e0f58cec68c95ae624dac1d5dea85cdf3`  
		Last Modified: Wed, 13 May 2020 18:57:17 GMT  
		Size: 6.1 MB (6052326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:decd0784e7c5c466738e00e0ec516f47418af7bb8767a491b9cd69528ccd9774`  
		Last Modified: Wed, 13 May 2020 18:57:15 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8d1a3559a70a9763211265e9542225cb42f7e773fa437b82c2290c7446a6a9`  
		Last Modified: Wed, 13 May 2020 18:57:15 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
