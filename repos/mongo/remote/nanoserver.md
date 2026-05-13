## `mongo:nanoserver`

```console
$ docker pull mongo@sha256:56b496248c36de93a4aaf1adda32c394eeb203b98068ed277cb811e3b25fe2a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `mongo:nanoserver` - windows version 10.0.20348.5139; amd64

```console
$ docker pull mongo@sha256:df7a5074597a37f37305751db4b833b721f6728efc1b450ba56c0e6eb7a6ae49
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.2 MB (944212088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78dc6498b6e19b350d9601d56d1f680544327e320259a87fe39651801936b1e3`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 13 May 2026 00:27:10 GMT
SHELL [cmd /S /C]
# Wed, 13 May 2026 00:27:13 GMT
USER ContainerAdministrator
# Wed, 13 May 2026 00:27:15 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 13 May 2026 00:27:15 GMT
USER ContainerUser
# Wed, 13 May 2026 00:27:16 GMT
COPY multi:540d6dd70b1e7484f1958dc08b337aeb56cf8a92fe38be4c279dd406990d6935 in C:\Windows\System32\ 
# Wed, 13 May 2026 00:27:16 GMT
ENV MONGO_VERSION=8.2.7
# Wed, 13 May 2026 00:28:06 GMT
COPY dir:ca1e02e68022d449b9840dfa05212532d650698fb89c8dc0f159478e5e32fba5 in C:\mongodb 
# Wed, 13 May 2026 00:28:26 GMT
RUN mongod --version
# Wed, 13 May 2026 00:28:26 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 13 May 2026 00:28:26 GMT
EXPOSE 27017
# Wed, 13 May 2026 00:28:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cc421edb4cc2a4019979092ebbc8340e9663f7b2e627fab29f8266f0feb386`  
		Last Modified: Wed, 13 May 2026 00:28:34 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd97e23ed96d0a330260a8853e4686eb11c87fde78bc937c38025907dd924af0`  
		Last Modified: Wed, 13 May 2026 00:28:34 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fdfa5fbcb153be0b65564c421f343be639fdb526ec37f960c3845ac12033490`  
		Last Modified: Wed, 13 May 2026 00:28:33 GMT  
		Size: 77.4 KB (77364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01e6b47f0820021a58ad929bef6bb4f5f3aaa23665c27135625e8f863748b7b`  
		Last Modified: Wed, 13 May 2026 00:28:33 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13adaf70f6c8c806cd8ef59cd781aeb9159456dcca5cf1a18376141ee1c3100`  
		Last Modified: Wed, 13 May 2026 00:28:33 GMT  
		Size: 275.2 KB (275181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012494111556450c24621dc72c3e0a96fb7f90b57516c6fbf3d4711aa68691fc`  
		Last Modified: Wed, 13 May 2026 00:28:32 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b32f2616be7c665cc29306ce442479f3f85502a7c32240e089ddb0c68d9f994`  
		Last Modified: Wed, 13 May 2026 00:29:58 GMT  
		Size: 816.7 MB (816724070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc11a74d95edac52000a612450e6d44b5ef5a48a645f66ad2f79a4fc1d994033`  
		Last Modified: Wed, 13 May 2026 00:28:31 GMT  
		Size: 89.3 KB (89283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57058134aee959e3c203bf6fac1ee8224ad340bb1e7a069095ad24042b0e0128`  
		Last Modified: Wed, 13 May 2026 00:28:31 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb86a69b7720f33b74339c7981aec73df0dadd9459a86a0cf634304fb415734`  
		Last Modified: Wed, 13 May 2026 00:28:31 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab6d74e60060c15dfebf33760bed7caf09046a6b306c5f55441a3a556017b5e`  
		Last Modified: Wed, 13 May 2026 00:28:31 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
