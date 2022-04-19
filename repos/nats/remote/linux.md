## `nats:linux`

```console
$ docker pull nats@sha256:7097e49629a8b62974eb8b4577ef5b9b9867abd6367771ac3a963ffeef1865fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:8bd17688b3f48c3adfdab56d3effce03a361b1b47504f2e1e7350d59cd9daab2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4577760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d46ec68770eafbc93e836c7ec9872d55f6bfd6fb2af492abe4534b795547f6f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Apr 2022 03:06:10 GMT
COPY file:ca37028b27d839d950bcae33931d7e6615fb1b09323703fcf9eaa9647f444002 in /nats-server 
# Tue, 19 Apr 2022 03:06:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 19 Apr 2022 03:06:10 GMT
EXPOSE 4222 6222 8222
# Tue, 19 Apr 2022 03:06:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 19 Apr 2022 03:06:10 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 19 Apr 2022 03:06:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e9fc57d876d27155804078e28290d22cbba732762320a4daca2d681be9d5ac56`  
		Last Modified: Tue, 19 Apr 2022 03:06:58 GMT  
		Size: 4.6 MB (4577253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953499f4b34cabe7f9d88476ba63999880bf8aff1c88038d2fc6eb9c1c846b13`  
		Last Modified: Tue, 19 Apr 2022 03:06:57 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:f1d583764567c881a0e61a2f17281162dd765f00db2474de4081a2b643e3d4c5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4236615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af0f20fc23cdefbee46926169caa559e7a84f9204347b6426f377b91c9b69f27`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Apr 2022 01:55:37 GMT
COPY file:8cee33100ded62c397ffde3de5e9ea249d650168c802e2611fea578c07655f04 in /nats-server 
# Tue, 19 Apr 2022 01:55:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 19 Apr 2022 01:55:38 GMT
EXPOSE 4222 6222 8222
# Tue, 19 Apr 2022 01:55:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 19 Apr 2022 01:55:39 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 19 Apr 2022 01:55:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41d693eff09d55c2616a7901f894d0d0f2498f5f28e23f3a863919e02e22a6ad`  
		Last Modified: Tue, 19 Apr 2022 01:57:59 GMT  
		Size: 4.2 MB (4236107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b54f80cb9d96012058f10a179ecd81de8d5505556b318b2400d3294ba4a9e9`  
		Last Modified: Tue, 19 Apr 2022 01:57:57 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:ed87fc96ebeace8ad252ad368ab68f1ef976daadae90f50d8f1f917364b8050c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c348e474d9b30a28b01ce9d8566ee12c3404e1a91cddfa31c8de44ba3c6b495b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 09 Mar 2022 23:26:11 GMT
COPY file:143b3802bb689cd4b4badd2b1463feaa3881f20e6fd303b203aa25ea206fb684 in /nats-server 
# Wed, 09 Mar 2022 23:26:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 09 Mar 2022 23:26:12 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 23:26:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 09 Mar 2022 23:26:13 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 09 Mar 2022 23:26:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c0d2f46ac12a6f6109f1f810a72658a0faa0b7301dfa2abc4f222012bab43639`  
		Last Modified: Wed, 09 Mar 2022 23:28:32 GMT  
		Size: 4.2 MB (4168878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4e39b35a6f91da4330c0e57dcc7c9e91270e4d54cf1097b98ad3ab1a1ca178`  
		Last Modified: Wed, 09 Mar 2022 23:28:29 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:92166da3897fa629b266a687308aee6da5d6a56a53a7b7bfd11009d8fec7c832
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4215629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:622c4d607a2904fcea14a3b16b7c03c48cdbdc478a0d97fd80e79d6748b2767d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Apr 2022 03:28:46 GMT
COPY file:05c214eeb4e75353a7b7b920d3a6c8e8ae2768c0f9d965745307feda489dfdf1 in /nats-server 
# Tue, 19 Apr 2022 03:28:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 19 Apr 2022 03:28:47 GMT
EXPOSE 4222 6222 8222
# Tue, 19 Apr 2022 03:28:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 19 Apr 2022 03:28:49 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 19 Apr 2022 03:28:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5c1abcb1fd5645c2333d0ec9f6ffab7e85b00554c29b70f6bfc2d8d18b9e8bb2`  
		Last Modified: Tue, 19 Apr 2022 03:30:06 GMT  
		Size: 4.2 MB (4215121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c98a93bee8cca0be2d741c7d90d5de238ba658cba0c41f37b42566e08a0442`  
		Last Modified: Tue, 19 Apr 2022 03:30:06 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
