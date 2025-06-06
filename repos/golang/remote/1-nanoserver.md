## `golang:1-nanoserver`

```console
$ docker pull golang@sha256:f63088bc9684f989111c2baf378a699734b709fcd03169dc3b25f9a9b52c7038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64

### `golang:1-nanoserver` - windows version 10.0.26100.4061; amd64

```console
$ docker pull golang@sha256:723cfa820fc4ecbf65da182523d1059a5e24b8696affb24d4b69638110788e5d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273494363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958a97b53817c546ae5c1663568227d0bca548c7149b970dd9aaa8053dde1daa`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 10 May 2025 00:58:48 GMT
RUN Apply image 10.0.26100.4061
# Thu, 05 Jun 2025 20:06:13 GMT
SHELL [cmd /S /C]
# Thu, 05 Jun 2025 20:06:14 GMT
ENV GOPATH=C:\go
# Thu, 05 Jun 2025 20:06:15 GMT
USER ContainerAdministrator
# Thu, 05 Jun 2025 20:06:17 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Thu, 05 Jun 2025 20:06:17 GMT
USER ContainerUser
# Thu, 05 Jun 2025 20:06:18 GMT
ENV GOLANG_VERSION=1.24.4
# Thu, 05 Jun 2025 20:07:23 GMT
COPY dir:70f015619b03b14f09ca45829787e7bb802d481fe7480466582aed33ddb74b24 in C:\Program Files\Go 
# Thu, 05 Jun 2025 20:07:26 GMT
RUN go version
# Thu, 05 Jun 2025 20:07:26 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:9824510349be04d2eb26f9aaba1d016eddcbed10bdcd6681f4636c948766f3d1`  
		Last Modified: Thu, 15 May 2025 20:15:30 GMT  
		Size: 191.4 MB (191412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96871aa7715290f86b2e79812fda829f774100452f7da8fd3ad30af2f163bb75`  
		Last Modified: Thu, 05 Jun 2025 20:12:55 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64acc29cd5a2336e7b95f6cb760dfb09fd3c217596e7996f9a44ecc9ff140cbf`  
		Last Modified: Thu, 05 Jun 2025 20:12:59 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2a6d65115a0aca1d9f17661f5f1b5be2961f47f2e5002d27d37c6ede3e37a7`  
		Last Modified: Thu, 05 Jun 2025 20:13:01 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d7b87cbaa9b9afa73cd2ca00684515414c89ca9694c3dac33f79dbdd6d1f5a`  
		Last Modified: Thu, 05 Jun 2025 20:13:07 GMT  
		Size: 76.3 KB (76276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6439ce219f0dcb24246fea8e4541c647606304dcd8e398528626b5416a8f99e0`  
		Last Modified: Thu, 05 Jun 2025 20:13:15 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768754130826bcab12a19ed7088e4f99c9beb9de130a5a96423fc59a6a6efda4`  
		Last Modified: Thu, 05 Jun 2025 20:13:18 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae75b0e29efddd83918929383dbd53cf6c3ee5bd76ff1cbc236cce98e4593529`  
		Last Modified: Thu, 05 Jun 2025 23:22:44 GMT  
		Size: 81.9 MB (81911360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e365cdc888dc0041647bf59b21f81ae5ba63a2ab102b938d3de3f722d275a2`  
		Last Modified: Thu, 05 Jun 2025 20:13:22 GMT  
		Size: 88.1 KB (88121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8715e3568eab5c6a07043d7781728ad4a125e7bded37f7be3538fbf4a2d32b3d`  
		Last Modified: Thu, 05 Jun 2025 20:13:27 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-nanoserver` - windows version 10.0.20348.3692; amd64

```console
$ docker pull golang@sha256:2864abdfcc345e4404101dc29772dcca862897d383b8f4d1a0f2d230f1e530c7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.6 MB (204612566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06b89d54d1e2bb6e6d8ba4e1f412435806d7ea4841b57b5ef8b948748ab8ac25`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Thu, 05 Jun 2025 20:01:32 GMT
SHELL [cmd /S /C]
# Thu, 05 Jun 2025 20:01:33 GMT
ENV GOPATH=C:\go
# Thu, 05 Jun 2025 20:01:34 GMT
USER ContainerAdministrator
# Thu, 05 Jun 2025 20:01:39 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Thu, 05 Jun 2025 20:01:40 GMT
USER ContainerUser
# Thu, 05 Jun 2025 20:01:41 GMT
ENV GOLANG_VERSION=1.24.4
# Thu, 05 Jun 2025 20:02:49 GMT
COPY dir:70f015619b03b14f09ca45829787e7bb802d481fe7480466582aed33ddb74b24 in C:\Program Files\Go 
# Thu, 05 Jun 2025 20:02:53 GMT
RUN go version
# Thu, 05 Jun 2025 20:02:54 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749b28e6e2e0377a25383079b7f7821e3685ada6edaef7379cdaa0e78b4b99ae`  
		Last Modified: Thu, 05 Jun 2025 20:03:53 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fcd0a1af75e72ff08748923235bb8d8fd0b7882cbffbc3fc601f27a0a5866ac`  
		Last Modified: Thu, 05 Jun 2025 20:03:54 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0387b69b4474ac221469ecb0401045dbfed73d4d958d3358618032d467595072`  
		Last Modified: Thu, 05 Jun 2025 20:13:02 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cea18c2e3a32f38a623e314d18004a897e628fad41aa24427de9e84b914320b`  
		Last Modified: Thu, 05 Jun 2025 20:13:05 GMT  
		Size: 73.6 KB (73642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8547d9f3509c3d8d6f3b1b63c60a280184e3e9c44ba5ba9b6e5508ff6d4bc`  
		Last Modified: Thu, 05 Jun 2025 20:13:09 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0928f94ba5f63e9d82a4718299c8dc5aedf52555cecc2cdec97e3f3130d0b977`  
		Last Modified: Thu, 05 Jun 2025 20:13:12 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734a9a36f07cc32054f2ffde0cd6d8bf072786c47f11faec01f2a32c74659bd9`  
		Last Modified: Thu, 05 Jun 2025 20:25:27 GMT  
		Size: 81.9 MB (81878314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c032fa6869fe2f1c10489952297d788667bcde2867f22e609e6f0a9377e9b0d6`  
		Last Modified: Thu, 05 Jun 2025 20:13:16 GMT  
		Size: 77.5 KB (77541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed9a81f96386036fa1a8bf0db26f3cdd44ea1f8e84cea337efecb8587ea9d663`  
		Last Modified: Thu, 05 Jun 2025 20:13:22 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
