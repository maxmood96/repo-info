## `mongo:8-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:f5621c9aed9e4d3f5518317ce6797d85becdfe7f09640bcd79fc1740e43e5352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `mongo:8-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull mongo@sha256:a6ee4a4ad0827b59d997a5cba4311e08c4a312d9ccb12afe3aafbe4f96f31104
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **940.7 MB (940707238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2769cc4149f8f6b657b0b2139a5a79848f417ec2ae1c46153710fe4f8e43206`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 09 Dec 2025 21:14:54 GMT
SHELL [cmd /S /C]
# Tue, 09 Dec 2025 21:14:54 GMT
USER ContainerAdministrator
# Tue, 09 Dec 2025 21:14:56 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Tue, 09 Dec 2025 21:14:57 GMT
USER ContainerUser
# Tue, 09 Dec 2025 21:14:57 GMT
COPY multi:540d6dd70b1e7484f1958dc08b337aeb56cf8a92fe38be4c279dd406990d6935 in C:\Windows\System32\ 
# Tue, 09 Dec 2025 21:14:58 GMT
ENV MONGO_VERSION=8.2.2
# Tue, 09 Dec 2025 21:15:37 GMT
COPY dir:34b17986dc7f69da0f0036b088796e7e44f1eda590d700b8613e7d7fcb8f43d9 in C:\mongodb 
# Tue, 09 Dec 2025 21:16:04 GMT
RUN mongod --version
# Tue, 09 Dec 2025 21:16:04 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 09 Dec 2025 21:16:04 GMT
EXPOSE 27017
# Tue, 09 Dec 2025 21:16:05 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367086539ef00c4c8cb1a5d443fde51b5658976e1ee57f552b101bea036c7f51`  
		Last Modified: Tue, 09 Dec 2025 21:17:31 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce63405a9229eea2709e1824c6bf227e8230b828ddd54cdfe148e4b23693e20`  
		Last Modified: Tue, 09 Dec 2025 21:17:31 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45602e9167d48b1d4219984bfce5757c320cee6a66cc0a28a8d55fadf4682176`  
		Last Modified: Tue, 09 Dec 2025 21:17:31 GMT  
		Size: 78.2 KB (78192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4945380fbe9e7bdafcc0ac69dd3a147593da9ed1478a635900c269211cbef7`  
		Last Modified: Tue, 09 Dec 2025 21:17:31 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db9aad7b458298ce2f4ad3725ca00880f4ad0cd6332f9840222c147107faa2c5`  
		Last Modified: Tue, 09 Dec 2025 21:17:31 GMT  
		Size: 275.2 KB (275202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d760e9b46c80f00b223954db7981abbed5e930e8f048807dab209cea69ef4bd6`  
		Last Modified: Tue, 09 Dec 2025 21:17:31 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b9a7ea5028c9b8158e7b840735e3ddac0a04da04195d0e0d98ccaa029e9687`  
		Last Modified: Tue, 09 Dec 2025 21:17:52 GMT  
		Size: 813.9 MB (813906871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38169236e22982abb29c0e184d2a1276aa7d1cf5e2f4009ae5c2e9abd732ef2a`  
		Last Modified: Tue, 09 Dec 2025 21:17:31 GMT  
		Size: 81.3 KB (81264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beaac38cae3c4b86ee70447a55d41c96400b0b9a0b85892d81fd31d2770751fa`  
		Last Modified: Tue, 09 Dec 2025 21:17:31 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8986309a7e8dc11c0ea82aa3fb023f99f9c5d4a018e72ace44b6bca4b91f0821`  
		Last Modified: Tue, 09 Dec 2025 21:17:32 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4d6ff0df54e73f4f374ed8ab141a43bf474ed45beb364a5cc9035ef56a4a31`  
		Last Modified: Tue, 09 Dec 2025 21:17:32 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
