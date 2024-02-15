## `mongo:nanoserver`

```console
$ docker pull mongo@sha256:8015ed6bcf7d1b5ef533e00dc53b07789abefcd3bae189948e9951d5a26d8efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `mongo:nanoserver` - windows version 10.0.20348.2322; amd64

```console
$ docker pull mongo@sha256:3de2c37de08aae9195f0d6a3c1aa637e03608ebcaba4bee17b9875e21b8bc838
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **732.9 MB (732866476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7393d466812b2da25c6dce08593de1167335083d9e9566f44c381b9d8fe56c6a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 07 Feb 2024 06:29:10 GMT
RUN Apply image 10.0.20348.2322
# Wed, 14 Feb 2024 20:59:05 GMT
SHELL [cmd /S /C]
# Wed, 14 Feb 2024 20:59:05 GMT
USER ContainerAdministrator
# Wed, 14 Feb 2024 20:59:07 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 14 Feb 2024 20:59:08 GMT
USER ContainerUser
# Wed, 14 Feb 2024 20:59:09 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Wed, 14 Feb 2024 20:59:10 GMT
ENV MONGO_VERSION=7.0.5
# Wed, 14 Feb 2024 20:59:35 GMT
COPY dir:e35779bad98800653cfb4a4e0e8010143d34591b7f537faf64c0de91cf35eb83 in C:\mongodb 
# Wed, 14 Feb 2024 20:59:53 GMT
RUN mongod --version
# Wed, 14 Feb 2024 20:59:54 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 14 Feb 2024 20:59:54 GMT
EXPOSE 27017
# Wed, 14 Feb 2024 20:59:55 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:ccff18da882d371921351307d169380d3ac22ef981f2bb4f14fb2b332b395439`  
		Last Modified: Tue, 13 Feb 2024 23:39:47 GMT  
		Size: 120.7 MB (120735093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64736d518f4de739015c0bf7729048f353db3348974ec4e526c33054c789de51`  
		Last Modified: Wed, 14 Feb 2024 21:00:05 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a21d2577070e6ad2194ee4836bf849aeae3268dc272f9c59067cbe57d59f21`  
		Last Modified: Wed, 14 Feb 2024 21:00:05 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93bcc6099f4fb23b017d08fc41a8430c9f4e4f05928a26b293eca6ec2019789a`  
		Last Modified: Wed, 14 Feb 2024 21:00:01 GMT  
		Size: 79.2 KB (79150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0de6590ca9be4f8f2b5ac4e53633a4989bdf0aed91e307a34e283b26b47f13c`  
		Last Modified: Wed, 14 Feb 2024 21:00:01 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8daed6290b5bf80365e5fb7947dcec39b62a4dced043024183e1e5732f02613`  
		Last Modified: Wed, 14 Feb 2024 21:00:01 GMT  
		Size: 267.1 KB (267074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1178ab3f6e11d127a612288694d43a40bb14a6d5e4baacb3e3a36e46bd1a6081`  
		Last Modified: Wed, 14 Feb 2024 21:00:01 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc7573372ceab9a79d2a4d63bd8cfd50e845689e6b66a445bf88773ccb47440`  
		Last Modified: Wed, 14 Feb 2024 21:00:48 GMT  
		Size: 611.7 MB (611671771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770845c75e54ac43d9ae1e6a627a42a624e2783a10af9cc68583771d1b29ba68`  
		Last Modified: Wed, 14 Feb 2024 20:59:59 GMT  
		Size: 106.1 KB (106102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6ca0256c6cc998a75ce1e7d95c6a23ba8c1da78af6bc5ccdc585666f2c0187`  
		Last Modified: Wed, 14 Feb 2024 20:59:59 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c3973688979b587976ba827a35ff92342e7f2eff9fde41cf8e964623cb69f4`  
		Last Modified: Wed, 14 Feb 2024 20:59:59 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f55bc2d8f0ac2cd7f7f29bb7b1c5f366ec0aa0480de514b2a0cc978c42eaff0`  
		Last Modified: Wed, 14 Feb 2024 20:59:59 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:nanoserver` - windows version 10.0.17763.5458; amd64

```console
$ docker pull mongo@sha256:a484af1ba3f8a27a85eed59845a25ce83b9669d7f1da342a02ca2eeae3872790
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.7 MB (716727710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee51a9c8e697c17a35efd1b230a72a7068d6bb3802a0248d55e9c5409a3bc7b3`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 21:01:42 GMT
SHELL [cmd /S /C]
# Wed, 14 Feb 2024 21:01:44 GMT
USER ContainerAdministrator
# Wed, 14 Feb 2024 21:01:47 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 14 Feb 2024 21:01:48 GMT
USER ContainerUser
# Wed, 14 Feb 2024 21:01:49 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Wed, 14 Feb 2024 21:01:50 GMT
ENV MONGO_VERSION=7.0.5
# Wed, 14 Feb 2024 21:02:29 GMT
COPY dir:e35779bad98800653cfb4a4e0e8010143d34591b7f537faf64c0de91cf35eb83 in C:\mongodb 
# Wed, 14 Feb 2024 21:02:38 GMT
RUN mongod --version
# Wed, 14 Feb 2024 21:02:39 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 14 Feb 2024 21:02:40 GMT
EXPOSE 27017
# Wed, 14 Feb 2024 21:02:40 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe48b9a07140671f1fce94c9ab7d0b796fe3fba9296f97d601b0ace72550a4c`  
		Last Modified: Wed, 14 Feb 2024 21:02:46 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5aa426a4faf7683a83961f492e8cc3d8ace6880ffd97cd6f8f0b5090e7a930`  
		Last Modified: Wed, 14 Feb 2024 21:02:46 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cef3d6675cda69a538bd9bd8ae8d4529e77369945d6dc673aceb2f756410a9c`  
		Last Modified: Wed, 14 Feb 2024 21:02:45 GMT  
		Size: 83.8 KB (83763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc4513f9fece637fe9fd3320e597aaa2d379c74a975eef26e92d18f859c0ea0`  
		Last Modified: Wed, 14 Feb 2024 21:02:45 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:535e699d593d2944053f695de735482d35a8d5831665bf5b0a37632ca351ac15`  
		Last Modified: Wed, 14 Feb 2024 21:02:44 GMT  
		Size: 267.1 KB (267072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfaadf381281238a5a9e893d6e029a3b6aad5db694211a3e6f25da23ff7327e`  
		Last Modified: Wed, 14 Feb 2024 21:02:45 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6f363e1c8728cebd6b7b1c6f2e7cf2de88e587f4c1aee37b263c818a015708`  
		Last Modified: Wed, 14 Feb 2024 21:03:32 GMT  
		Size: 611.7 MB (611671774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43137a3a66349b7f35a8c687e07daf1f7775fbb4a39ae420b217e06b27332837`  
		Last Modified: Wed, 14 Feb 2024 21:02:43 GMT  
		Size: 76.2 KB (76236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ad6e9771c407aa0d93070d9ba3a66a6875c069d31c61b98fec53ab0d2e82b0`  
		Last Modified: Wed, 14 Feb 2024 21:02:43 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8814118791a0eb9b47d12cd7752e01e3f03ae0db2f7ead6acf732e7bc0f26ed`  
		Last Modified: Wed, 14 Feb 2024 21:02:43 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:546e59f06af4f384b8622789a9f9625c0275a96a9641f2560ed09a442e798dd2`  
		Last Modified: Wed, 14 Feb 2024 21:02:43 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
