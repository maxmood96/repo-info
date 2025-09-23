## `mongo:nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:d8f1ffb1be06f14084749fdb8d62b04424ee09c53d5b0b5adca784cbdd9b33e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `mongo:nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull mongo@sha256:cdc29e799ade3833f719f6f9893afea9485a50432a79d545cbed2fe3d2c81c89
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **906.5 MB (906537461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:184cb8b1acac18115dc25f4c0eb1432fe9d118d6435177631cfc4744f02d061f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Mon, 22 Sep 2025 23:13:19 GMT
SHELL [cmd /S /C]
# Mon, 22 Sep 2025 23:13:20 GMT
USER ContainerAdministrator
# Mon, 22 Sep 2025 23:13:29 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Mon, 22 Sep 2025 23:13:30 GMT
USER ContainerUser
# Mon, 22 Sep 2025 23:13:32 GMT
COPY multi:540d6dd70b1e7484f1958dc08b337aeb56cf8a92fe38be4c279dd406990d6935 in C:\Windows\System32\ 
# Mon, 22 Sep 2025 23:13:33 GMT
ENV MONGO_VERSION=8.0.14
# Mon, 22 Sep 2025 23:16:57 GMT
COPY dir:37e292869e31a568e183c4d0de70515dd614bd5c09bb4c5808f7c1587ef98689 in C:\mongodb 
# Mon, 22 Sep 2025 23:17:24 GMT
RUN mongod --version
# Mon, 22 Sep 2025 23:17:25 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 22 Sep 2025 23:17:26 GMT
EXPOSE 27017
# Mon, 22 Sep 2025 23:17:26 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a70b099237d05ac8a76a52a4c3532b891073e3ba9cc808f152379352a7ba11`  
		Last Modified: Mon, 22 Sep 2025 23:19:01 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89781f2f81f9fd71ec844060f30dc242686f7d95d05002693d2c17b684c8f6e7`  
		Last Modified: Mon, 22 Sep 2025 23:19:01 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685f0d3a0152917103b83f71c6c3de0a40d6b2ce799eeec29ec68c7e87339814`  
		Last Modified: Mon, 22 Sep 2025 23:19:01 GMT  
		Size: 86.1 KB (86062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b08bef6be3f2a44bed65cea54aa3a6988a3870b11c2c104ffc66dd5a94cb4c`  
		Last Modified: Mon, 22 Sep 2025 23:19:01 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29bbded00dadc74351585e38ade8b6dce03493d6a878dc2aa0a9f5913a6d791`  
		Last Modified: Mon, 22 Sep 2025 23:19:01 GMT  
		Size: 275.2 KB (275211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5487fa6fa9c75f900455407b36f05d84f23fd62dd205da5633bdd1c10288f3a6`  
		Last Modified: Mon, 22 Sep 2025 23:19:01 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13193a3abdf674c49d49f656661e1156e3f7156e424291d13dcf021b670c4ce8`  
		Last Modified: Tue, 23 Sep 2025 01:08:20 GMT  
		Size: 783.4 MB (783362598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c44276430f7d99e2f9e667ab6b722ad88445bcb6e3be002c839a931f0a995b`  
		Last Modified: Mon, 22 Sep 2025 23:19:02 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba4028d2124d3eabfd57d26f3d091fc74a38544cde9167b3b0c3c81ace2fb876`  
		Last Modified: Mon, 22 Sep 2025 23:19:02 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb58ebb4e2493d5d936d21c4e7fb942e97f9ce0c615e56f0f63d9f428071a13`  
		Last Modified: Mon, 22 Sep 2025 23:19:02 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e1020fe3606bc4267a34a837e200d6613d5407d3a836da7c9018760678534a`  
		Last Modified: Mon, 22 Sep 2025 23:19:02 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
