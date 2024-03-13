<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.19`](#nats2-alpine319)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2.10`](#nats210)
-	[`nats:2.10-alpine`](#nats210-alpine)
-	[`nats:2.10-alpine3.19`](#nats210-alpine319)
-	[`nats:2.10-linux`](#nats210-linux)
-	[`nats:2.10-nanoserver`](#nats210-nanoserver)
-	[`nats:2.10-nanoserver-1809`](#nats210-nanoserver-1809)
-	[`nats:2.10-scratch`](#nats210-scratch)
-	[`nats:2.10-windowsservercore`](#nats210-windowsservercore)
-	[`nats:2.10-windowsservercore-1809`](#nats210-windowsservercore-1809)
-	[`nats:2.10.12`](#nats21012)
-	[`nats:2.10.12-alpine`](#nats21012-alpine)
-	[`nats:2.10.12-alpine3.19`](#nats21012-alpine319)
-	[`nats:2.10.12-linux`](#nats21012-linux)
-	[`nats:2.10.12-nanoserver`](#nats21012-nanoserver)
-	[`nats:2.10.12-nanoserver-1809`](#nats21012-nanoserver-1809)
-	[`nats:2.10.12-scratch`](#nats21012-scratch)
-	[`nats:2.10.12-windowsservercore`](#nats21012-windowsservercore)
-	[`nats:2.10.12-windowsservercore-1809`](#nats21012-windowsservercore-1809)
-	[`nats:2.9`](#nats29)
-	[`nats:2.9-alpine`](#nats29-alpine)
-	[`nats:2.9-alpine3.18`](#nats29-alpine318)
-	[`nats:2.9-linux`](#nats29-linux)
-	[`nats:2.9-nanoserver`](#nats29-nanoserver)
-	[`nats:2.9-nanoserver-1809`](#nats29-nanoserver-1809)
-	[`nats:2.9-scratch`](#nats29-scratch)
-	[`nats:2.9-windowsservercore`](#nats29-windowsservercore)
-	[`nats:2.9-windowsservercore-1809`](#nats29-windowsservercore-1809)
-	[`nats:2.9.25`](#nats2925)
-	[`nats:2.9.25-alpine`](#nats2925-alpine)
-	[`nats:2.9.25-alpine3.18`](#nats2925-alpine318)
-	[`nats:2.9.25-linux`](#nats2925-linux)
-	[`nats:2.9.25-nanoserver`](#nats2925-nanoserver)
-	[`nats:2.9.25-nanoserver-1809`](#nats2925-nanoserver-1809)
-	[`nats:2.9.25-scratch`](#nats2925-scratch)
-	[`nats:2.9.25-windowsservercore`](#nats2925-windowsservercore)
-	[`nats:2.9.25-windowsservercore-1809`](#nats2925-windowsservercore-1809)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.19`](#natsalpine319)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)

## `nats:2`

```console
$ docker pull nats@sha256:9b1ee0caf5737f6b44b15da670b866900af4077d6ae6e2a170466e2e0fc68cb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5576; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:6fb1a85021a8411e0470cca8a43d461db915d2df605657389c4f0595d2e42e91
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5548142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8780d448219e4996eb219326ba6943b7e05f04ab1189a6f1dcf2e013058e3e36`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:47:57 GMT
COPY file:33d3e4ce6e17dc907ca0b478996354d26d433431b7bf48ae5bef3ec2ea1359f1 in /nats-server 
# Wed, 13 Mar 2024 01:47:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:47:57 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:47:57 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:47:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce8539fabe7af34129953a073c64515d008d19eac52a820ef52368f6411e540d`  
		Last Modified: Wed, 13 Mar 2024 01:48:46 GMT  
		Size: 5.5 MB (5547633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5208dae10516783bd9b5be071d7f3d39c84e1138b3887856c85f570ec4f588c`  
		Last Modified: Wed, 13 Mar 2024 01:48:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:b717fb731a88e81bdabf9b7eb28e2ee0fa423ff801dcd5819fb4ffaf217cb208
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5263761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51552a7d22c2c5ca2447ff2b4198de16cfdff9a116a3c54ef5af0d997a9469f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:49:35 GMT
COPY file:c24c6855bab6e8b64a222738f44249dd58afe5ec56a34cfd64493e736f5325df in /nats-server 
# Wed, 13 Mar 2024 00:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:49:35 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:49:35 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:49:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bc2b5fa4421ea8f446fd52c0a8e7c8c6e048dc4aa6a096fb60765aa281147267`  
		Last Modified: Wed, 13 Mar 2024 00:50:20 GMT  
		Size: 5.3 MB (5263253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652cf78472b592b1ea355485d1a353340ba41c0d01b26f15ffacc090db84d7bb`  
		Last Modified: Wed, 13 Mar 2024 00:50:19 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:07d02d1f567ff67a36ece1f90364e466f099db860d2e8ec1f2143bec1c3710f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5956a4e3835d4532ea5cbfc23f7b2e2d96d15a877f42392feea63afa16be107b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:35:52 GMT
COPY file:6899efa16d7091375dc53de2fc1e5686e82569d9799d6cede2e40b0a8b6abb48 in /nats-server 
# Wed, 13 Mar 2024 00:35:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:35:52 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:35:52 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:35:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:68296288971fdb3ddfe9bfba9b6a79725a69e891fb82cd5708f088afaac9929f`  
		Last Modified: Wed, 13 Mar 2024 00:36:43 GMT  
		Size: 5.3 MB (5254529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652026202bce83174144280de06b0537518e9d13e1674ac88f0d7e8491a2e440`  
		Last Modified: Wed, 13 Mar 2024 00:36:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f8017338e2c0dd9d3adb17672dd8226d475d5c810fa5f742c27a1d77f6e0c0e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8216507954fc8ffbaa79f3aa0908756fb3b5e699a13215671cf23837d30ca343`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:40:40 GMT
COPY file:674069719b01a345db55aa1ea35485a8b6f0cf0eed465ae05a0c00073e2ab2ab in /nats-server 
# Wed, 13 Mar 2024 00:40:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:40:40 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:40:40 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:40:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d5466aeaf1139b432e415e6412234c167a91220e74d17f50be1a2de5b0fb1b21`  
		Last Modified: Wed, 13 Mar 2024 00:41:26 GMT  
		Size: 5.1 MB (5117178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562c0bd40d1b70ec911e4b7219f7867675e2ad1c67899a3643f13d261d792187`  
		Last Modified: Wed, 13 Mar 2024 00:41:25 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; ppc64le

```console
$ docker pull nats@sha256:e964ace9a5047268966aa2f1f2e10472325f21ac790016722c0a9090997a39f1
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a273f9d6d6aa560ff8df97aee7e4c13f87044f2be0081b07ba0f4a0fafd81a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 16 Feb 2024 19:24:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:29:00 GMT
COPY file:0e1c98477f605478a27423b67d1c7bf88d4b2a56d0696ea31430a8a59b294dd8 in /nats-server 
# Wed, 13 Mar 2024 01:29:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:29:01 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:29:01 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:29:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7eaf17599ba122502fe00d1cb4014722df0b46a83f614f9430f71b816a6999f8`  
		Last Modified: Wed, 13 Mar 2024 01:29:44 GMT  
		Size: 5.1 MB (5096748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b8d7d148d9f2f60c0b13204daf3a2f76ff85991d79fe4fd82aa842a3d77a1d`  
		Last Modified: Wed, 13 Mar 2024 01:29:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:21d23f9777f88070c60ce8bf669dd9169ad10d91ddae1f43c02b5419cc5fcbc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5430830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a9daecac5ba461be180b94ca61fe053ebe1e5c23af8e61522f1854982e6157`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:15:09 GMT
COPY file:cc94c349de0e266f428d63773845fb669334304c5fbcffeec57553d333126f22 in /nats-server 
# Wed, 13 Mar 2024 01:15:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:15:09 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:15:09 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:15:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0bf838b872f1e012c580bbff8d1e66a09a7b05a85651db222851ea3323dab3d2`  
		Last Modified: Wed, 13 Mar 2024 01:16:47 GMT  
		Size: 5.4 MB (5430321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668de88817078f4ef2cf284dff428f40567f94b7132efee56fe3abe6264e6d42`  
		Last Modified: Wed, 13 Mar 2024 01:16:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats@sha256:1bb4572909b97a5aea3e76230e9d09a1078a21d41ba7000bd5afbe5225fc1568
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110290182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a1f3d16c6f5aea885d55ec76e40c984ca8763448ae4b9b424ec4d5bec24fc8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 02:21:55 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:21:57 GMT
RUN cmd /S /C #(nop) COPY file:b8b09037eca4c9daccbaf940396fb084777535cdce4ec562f44c0b727cf16e3e in C:\nats-server.exe 
# Wed, 13 Mar 2024 02:21:57 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Mar 2024 02:21:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 02:21:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Mar 2024 02:21:59 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e772fbc90f54f9eab2951a9615b88e9eca8fc78909aba2cb3678cc214eb88ae2`  
		Last Modified: Wed, 13 Mar 2024 02:26:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9cd82df1e1baf71960c98c3ca3996de090e25ce522c16d07628ea7705a1c7b`  
		Last Modified: Wed, 13 Mar 2024 02:26:26 GMT  
		Size: 5.7 MB (5663658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce47417df81557c57ff79790516751ae140155b5d06e2f8538fcf4d7e94a1004`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c07d5748899da1f68ed98e7331fa02c4175552921ad31f2ec6ba40f208c69d`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89220da9dce87f2d7ea149e170563fa7bac7ae732a1b8c89f51d60e5da18020e`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78635ce16de8337563a88c3a78835fed97c207dc9254d2dc0d06594b9926b0e0`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:7a3dedb2152d01809b0343a8fce27241d6eae68f65200a8e6da78d88ac4257a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:04333a656bd283d8642c365f790bbd26a0dd2919a0d29dd75998776c6ef7207d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9577940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606a0820025fa72d87e550430e7c14c89557b69fecac16e732dbf2d3c0bcaa76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 01:47:48 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 01:47:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 01:47:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 01:47:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 01:47:51 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:47:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 01:47:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a35673fda7fb893fc2c187357a17a1c13cb7b1958fa8d97eee3155901c44fba`  
		Last Modified: Wed, 13 Mar 2024 01:48:27 GMT  
		Size: 6.2 MB (6168214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdf5efdff66ae170a3b780d793b6b5d821138b53926474870aebccb2af5ee57`  
		Last Modified: Wed, 13 Mar 2024 01:48:25 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c95813002da682382a4ba34c5210071c10314593a044ab5120d5d8780b07e4a`  
		Last Modified: Wed, 13 Mar 2024 01:48:25 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:6e93abf037354dbe3af08ece7d516f8a4e61c675fbab84594adf10b108082777
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9051274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075217343e913477fcd44713b6ae36fa6c55e5a333eca26c9e952a97e51a14f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 00:49:24 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 00:49:28 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 00:49:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 00:49:28 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 00:49:28 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:49:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 00:49:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b7bd072e2424f96ed51dee5137cd95e43686fc4624f2d2feee365fd304f5fc`  
		Last Modified: Wed, 13 Mar 2024 00:50:00 GMT  
		Size: 5.9 MB (5884880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cd491dd798da6f6a27555feb3be80ea1e29262571e10acde00300ee332740f`  
		Last Modified: Wed, 13 Mar 2024 00:49:59 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568e37ef91f5962c31828a2adc1588dcec32dbe5859699372ff1656c5659a915`  
		Last Modified: Wed, 13 Mar 2024 00:49:59 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:06913e056cdc6c1997068e0fe2e6355f571c04f12afd48f9e02cea1f16554016
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8795654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fbc0f10b6a6c92c2a77318fa3a4f9b73f5dc9a8e0304b5475f614294196d6d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 00:35:35 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 00:35:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 00:35:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 00:35:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 00:35:39 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:35:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 00:35:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55a741d01acaf5448cb8ffa39243f9f34261fd88e914772554124224189cc81`  
		Last Modified: Wed, 13 Mar 2024 00:36:23 GMT  
		Size: 5.9 MB (5875752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d61266118e4acdda142cd2ac76a4ef35e24e7502ec60b4cf26cf49a145acdc`  
		Last Modified: Wed, 13 Mar 2024 00:36:18 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1e59e375c0cd803e4186b41a2566a69e1f0a8b88ba1cf0954a5a00d33af0d2`  
		Last Modified: Wed, 13 Mar 2024 00:36:18 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:62b700c1d94d9c9164795d902681026f20a4c2c215e70dea7661f632c43f93b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9088728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b8a7d9375b33a34c6019c8a05fc253872624aaba1066208fa1ae728471c370`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 00:40:21 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 00:40:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 00:40:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 00:40:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 00:40:24 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:40:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 00:40:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46909e9837d35c1cb85abbf0a81ed8df7ac00f9ac7df67d275bd7edb87fdc88b`  
		Last Modified: Wed, 13 Mar 2024 00:41:06 GMT  
		Size: 5.7 MB (5740016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a74044cf86ca3325a7a324fbd7d08694e721bad44f2f7865d35ed3b3ce23b4`  
		Last Modified: Wed, 13 Mar 2024 00:41:05 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f776b77a6001c5e0fd42db5610aa2acfeecb867c59a3559a2cd6983a5067ad6c`  
		Last Modified: Wed, 13 Mar 2024 00:41:05 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:e73b5c826fe9e8fc554f8e4440d8ae0504b4f7899d6c5bc38c6b68a0d9e705d0
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9078995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96541c86763ab33908efa9617f909b1b23853fc66f5740829aaa97d4fb819d4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 01:28:25 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 01:28:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 01:28:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 01:28:31 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 01:28:32 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:28:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 01:28:33 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd4d0c36112be2592baa66fdba8327cff756029be8e96f803015fce9a8bfab7`  
		Last Modified: Wed, 13 Mar 2024 01:29:22 GMT  
		Size: 5.7 MB (5719643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217c8e169d797596a8b822f912ec2ba564e491f6949ecd95a5a405d275c5a5a6`  
		Last Modified: Wed, 13 Mar 2024 01:29:21 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad20a946927156b80304d831d9d123a0ba902501570002869968e92231bbd32`  
		Last Modified: Wed, 13 Mar 2024 01:29:21 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:49f1c4fa564a8f8073315103db29d373273c7e703c43d6f275a1acc3ab010a3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9296162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7420d0049b07e2c363f050c33e0ac3ba0fe39fe6d0bee0ffea5c71f2fdf0749`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 01:14:00 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 01:14:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 01:14:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 01:14:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 01:14:03 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:14:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 01:14:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d4a8da7be6313cc596f154b85b638749ab970144f58575af5bef288a9e44ce`  
		Last Modified: Wed, 13 Mar 2024 01:16:34 GMT  
		Size: 6.1 MB (6052529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c87220ce1b5f8a7ed2e5ab6caf39ac9028ba6d25133711633f25a21b60c4b24`  
		Last Modified: Wed, 13 Mar 2024 01:16:33 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43f30dc994a90cc1c2a38e8a5176d279817dd3d25ffe3d8ac67b665c606f3b3`  
		Last Modified: Wed, 13 Mar 2024 01:16:33 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.19`

```console
$ docker pull nats@sha256:7a3dedb2152d01809b0343a8fce27241d6eae68f65200a8e6da78d88ac4257a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2-alpine3.19` - linux; amd64

```console
$ docker pull nats@sha256:04333a656bd283d8642c365f790bbd26a0dd2919a0d29dd75998776c6ef7207d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9577940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606a0820025fa72d87e550430e7c14c89557b69fecac16e732dbf2d3c0bcaa76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 01:47:48 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 01:47:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 01:47:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 01:47:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 01:47:51 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:47:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 01:47:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a35673fda7fb893fc2c187357a17a1c13cb7b1958fa8d97eee3155901c44fba`  
		Last Modified: Wed, 13 Mar 2024 01:48:27 GMT  
		Size: 6.2 MB (6168214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdf5efdff66ae170a3b780d793b6b5d821138b53926474870aebccb2af5ee57`  
		Last Modified: Wed, 13 Mar 2024 01:48:25 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c95813002da682382a4ba34c5210071c10314593a044ab5120d5d8780b07e4a`  
		Last Modified: Wed, 13 Mar 2024 01:48:25 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; arm variant v6

```console
$ docker pull nats@sha256:6e93abf037354dbe3af08ece7d516f8a4e61c675fbab84594adf10b108082777
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9051274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075217343e913477fcd44713b6ae36fa6c55e5a333eca26c9e952a97e51a14f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 00:49:24 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 00:49:28 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 00:49:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 00:49:28 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 00:49:28 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:49:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 00:49:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b7bd072e2424f96ed51dee5137cd95e43686fc4624f2d2feee365fd304f5fc`  
		Last Modified: Wed, 13 Mar 2024 00:50:00 GMT  
		Size: 5.9 MB (5884880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cd491dd798da6f6a27555feb3be80ea1e29262571e10acde00300ee332740f`  
		Last Modified: Wed, 13 Mar 2024 00:49:59 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568e37ef91f5962c31828a2adc1588dcec32dbe5859699372ff1656c5659a915`  
		Last Modified: Wed, 13 Mar 2024 00:49:59 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:06913e056cdc6c1997068e0fe2e6355f571c04f12afd48f9e02cea1f16554016
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8795654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fbc0f10b6a6c92c2a77318fa3a4f9b73f5dc9a8e0304b5475f614294196d6d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 00:35:35 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 00:35:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 00:35:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 00:35:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 00:35:39 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:35:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 00:35:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55a741d01acaf5448cb8ffa39243f9f34261fd88e914772554124224189cc81`  
		Last Modified: Wed, 13 Mar 2024 00:36:23 GMT  
		Size: 5.9 MB (5875752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d61266118e4acdda142cd2ac76a4ef35e24e7502ec60b4cf26cf49a145acdc`  
		Last Modified: Wed, 13 Mar 2024 00:36:18 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1e59e375c0cd803e4186b41a2566a69e1f0a8b88ba1cf0954a5a00d33af0d2`  
		Last Modified: Wed, 13 Mar 2024 00:36:18 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:62b700c1d94d9c9164795d902681026f20a4c2c215e70dea7661f632c43f93b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9088728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b8a7d9375b33a34c6019c8a05fc253872624aaba1066208fa1ae728471c370`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 00:40:21 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 00:40:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 00:40:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 00:40:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 00:40:24 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:40:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 00:40:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46909e9837d35c1cb85abbf0a81ed8df7ac00f9ac7df67d275bd7edb87fdc88b`  
		Last Modified: Wed, 13 Mar 2024 00:41:06 GMT  
		Size: 5.7 MB (5740016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a74044cf86ca3325a7a324fbd7d08694e721bad44f2f7865d35ed3b3ce23b4`  
		Last Modified: Wed, 13 Mar 2024 00:41:05 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f776b77a6001c5e0fd42db5610aa2acfeecb867c59a3559a2cd6983a5067ad6c`  
		Last Modified: Wed, 13 Mar 2024 00:41:05 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; ppc64le

```console
$ docker pull nats@sha256:e73b5c826fe9e8fc554f8e4440d8ae0504b4f7899d6c5bc38c6b68a0d9e705d0
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9078995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96541c86763ab33908efa9617f909b1b23853fc66f5740829aaa97d4fb819d4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 01:28:25 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 01:28:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 01:28:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 01:28:31 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 01:28:32 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:28:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 01:28:33 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd4d0c36112be2592baa66fdba8327cff756029be8e96f803015fce9a8bfab7`  
		Last Modified: Wed, 13 Mar 2024 01:29:22 GMT  
		Size: 5.7 MB (5719643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217c8e169d797596a8b822f912ec2ba564e491f6949ecd95a5a405d275c5a5a6`  
		Last Modified: Wed, 13 Mar 2024 01:29:21 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad20a946927156b80304d831d9d123a0ba902501570002869968e92231bbd32`  
		Last Modified: Wed, 13 Mar 2024 01:29:21 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; s390x

```console
$ docker pull nats@sha256:49f1c4fa564a8f8073315103db29d373273c7e703c43d6f275a1acc3ab010a3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9296162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7420d0049b07e2c363f050c33e0ac3ba0fe39fe6d0bee0ffea5c71f2fdf0749`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 01:14:00 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 01:14:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 01:14:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 01:14:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 01:14:03 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:14:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 01:14:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d4a8da7be6313cc596f154b85b638749ab970144f58575af5bef288a9e44ce`  
		Last Modified: Wed, 13 Mar 2024 01:16:34 GMT  
		Size: 6.1 MB (6052529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c87220ce1b5f8a7ed2e5ab6caf39ac9028ba6d25133711633f25a21b60c4b24`  
		Last Modified: Wed, 13 Mar 2024 01:16:33 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43f30dc994a90cc1c2a38e8a5176d279817dd3d25ffe3d8ac67b665c606f3b3`  
		Last Modified: Wed, 13 Mar 2024 01:16:33 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:bb90d21b87ba223e838d39e5ee66ebeea8b63e8a6bffb4a2b19f5b291e46d1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:6fb1a85021a8411e0470cca8a43d461db915d2df605657389c4f0595d2e42e91
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5548142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8780d448219e4996eb219326ba6943b7e05f04ab1189a6f1dcf2e013058e3e36`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:47:57 GMT
COPY file:33d3e4ce6e17dc907ca0b478996354d26d433431b7bf48ae5bef3ec2ea1359f1 in /nats-server 
# Wed, 13 Mar 2024 01:47:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:47:57 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:47:57 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:47:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce8539fabe7af34129953a073c64515d008d19eac52a820ef52368f6411e540d`  
		Last Modified: Wed, 13 Mar 2024 01:48:46 GMT  
		Size: 5.5 MB (5547633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5208dae10516783bd9b5be071d7f3d39c84e1138b3887856c85f570ec4f588c`  
		Last Modified: Wed, 13 Mar 2024 01:48:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:b717fb731a88e81bdabf9b7eb28e2ee0fa423ff801dcd5819fb4ffaf217cb208
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5263761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51552a7d22c2c5ca2447ff2b4198de16cfdff9a116a3c54ef5af0d997a9469f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:49:35 GMT
COPY file:c24c6855bab6e8b64a222738f44249dd58afe5ec56a34cfd64493e736f5325df in /nats-server 
# Wed, 13 Mar 2024 00:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:49:35 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:49:35 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:49:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bc2b5fa4421ea8f446fd52c0a8e7c8c6e048dc4aa6a096fb60765aa281147267`  
		Last Modified: Wed, 13 Mar 2024 00:50:20 GMT  
		Size: 5.3 MB (5263253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652cf78472b592b1ea355485d1a353340ba41c0d01b26f15ffacc090db84d7bb`  
		Last Modified: Wed, 13 Mar 2024 00:50:19 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:07d02d1f567ff67a36ece1f90364e466f099db860d2e8ec1f2143bec1c3710f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5956a4e3835d4532ea5cbfc23f7b2e2d96d15a877f42392feea63afa16be107b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:35:52 GMT
COPY file:6899efa16d7091375dc53de2fc1e5686e82569d9799d6cede2e40b0a8b6abb48 in /nats-server 
# Wed, 13 Mar 2024 00:35:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:35:52 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:35:52 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:35:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:68296288971fdb3ddfe9bfba9b6a79725a69e891fb82cd5708f088afaac9929f`  
		Last Modified: Wed, 13 Mar 2024 00:36:43 GMT  
		Size: 5.3 MB (5254529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652026202bce83174144280de06b0537518e9d13e1674ac88f0d7e8491a2e440`  
		Last Modified: Wed, 13 Mar 2024 00:36:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f8017338e2c0dd9d3adb17672dd8226d475d5c810fa5f742c27a1d77f6e0c0e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8216507954fc8ffbaa79f3aa0908756fb3b5e699a13215671cf23837d30ca343`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:40:40 GMT
COPY file:674069719b01a345db55aa1ea35485a8b6f0cf0eed465ae05a0c00073e2ab2ab in /nats-server 
# Wed, 13 Mar 2024 00:40:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:40:40 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:40:40 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:40:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d5466aeaf1139b432e415e6412234c167a91220e74d17f50be1a2de5b0fb1b21`  
		Last Modified: Wed, 13 Mar 2024 00:41:26 GMT  
		Size: 5.1 MB (5117178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562c0bd40d1b70ec911e4b7219f7867675e2ad1c67899a3643f13d261d792187`  
		Last Modified: Wed, 13 Mar 2024 00:41:25 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:e964ace9a5047268966aa2f1f2e10472325f21ac790016722c0a9090997a39f1
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a273f9d6d6aa560ff8df97aee7e4c13f87044f2be0081b07ba0f4a0fafd81a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 16 Feb 2024 19:24:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:29:00 GMT
COPY file:0e1c98477f605478a27423b67d1c7bf88d4b2a56d0696ea31430a8a59b294dd8 in /nats-server 
# Wed, 13 Mar 2024 01:29:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:29:01 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:29:01 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:29:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7eaf17599ba122502fe00d1cb4014722df0b46a83f614f9430f71b816a6999f8`  
		Last Modified: Wed, 13 Mar 2024 01:29:44 GMT  
		Size: 5.1 MB (5096748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b8d7d148d9f2f60c0b13204daf3a2f76ff85991d79fe4fd82aa842a3d77a1d`  
		Last Modified: Wed, 13 Mar 2024 01:29:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:21d23f9777f88070c60ce8bf669dd9169ad10d91ddae1f43c02b5419cc5fcbc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5430830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a9daecac5ba461be180b94ca61fe053ebe1e5c23af8e61522f1854982e6157`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:15:09 GMT
COPY file:cc94c349de0e266f428d63773845fb669334304c5fbcffeec57553d333126f22 in /nats-server 
# Wed, 13 Mar 2024 01:15:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:15:09 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:15:09 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:15:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0bf838b872f1e012c580bbff8d1e66a09a7b05a85651db222851ea3323dab3d2`  
		Last Modified: Wed, 13 Mar 2024 01:16:47 GMT  
		Size: 5.4 MB (5430321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668de88817078f4ef2cf284dff428f40567f94b7132efee56fe3abe6264e6d42`  
		Last Modified: Wed, 13 Mar 2024 01:16:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:38b381e6f2834d3c5120087f02c9d13f238a2142f54568a208fa74d554bb62d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats@sha256:1bb4572909b97a5aea3e76230e9d09a1078a21d41ba7000bd5afbe5225fc1568
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110290182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a1f3d16c6f5aea885d55ec76e40c984ca8763448ae4b9b424ec4d5bec24fc8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 02:21:55 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:21:57 GMT
RUN cmd /S /C #(nop) COPY file:b8b09037eca4c9daccbaf940396fb084777535cdce4ec562f44c0b727cf16e3e in C:\nats-server.exe 
# Wed, 13 Mar 2024 02:21:57 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Mar 2024 02:21:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 02:21:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Mar 2024 02:21:59 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e772fbc90f54f9eab2951a9615b88e9eca8fc78909aba2cb3678cc214eb88ae2`  
		Last Modified: Wed, 13 Mar 2024 02:26:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9cd82df1e1baf71960c98c3ca3996de090e25ce522c16d07628ea7705a1c7b`  
		Last Modified: Wed, 13 Mar 2024 02:26:26 GMT  
		Size: 5.7 MB (5663658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce47417df81557c57ff79790516751ae140155b5d06e2f8538fcf4d7e94a1004`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c07d5748899da1f68ed98e7331fa02c4175552921ad31f2ec6ba40f208c69d`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89220da9dce87f2d7ea149e170563fa7bac7ae732a1b8c89f51d60e5da18020e`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78635ce16de8337563a88c3a78835fed97c207dc9254d2dc0d06594b9926b0e0`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:38b381e6f2834d3c5120087f02c9d13f238a2142f54568a208fa74d554bb62d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats@sha256:1bb4572909b97a5aea3e76230e9d09a1078a21d41ba7000bd5afbe5225fc1568
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110290182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a1f3d16c6f5aea885d55ec76e40c984ca8763448ae4b9b424ec4d5bec24fc8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 02:21:55 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:21:57 GMT
RUN cmd /S /C #(nop) COPY file:b8b09037eca4c9daccbaf940396fb084777535cdce4ec562f44c0b727cf16e3e in C:\nats-server.exe 
# Wed, 13 Mar 2024 02:21:57 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Mar 2024 02:21:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 02:21:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Mar 2024 02:21:59 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e772fbc90f54f9eab2951a9615b88e9eca8fc78909aba2cb3678cc214eb88ae2`  
		Last Modified: Wed, 13 Mar 2024 02:26:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9cd82df1e1baf71960c98c3ca3996de090e25ce522c16d07628ea7705a1c7b`  
		Last Modified: Wed, 13 Mar 2024 02:26:26 GMT  
		Size: 5.7 MB (5663658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce47417df81557c57ff79790516751ae140155b5d06e2f8538fcf4d7e94a1004`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c07d5748899da1f68ed98e7331fa02c4175552921ad31f2ec6ba40f208c69d`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89220da9dce87f2d7ea149e170563fa7bac7ae732a1b8c89f51d60e5da18020e`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78635ce16de8337563a88c3a78835fed97c207dc9254d2dc0d06594b9926b0e0`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:bb90d21b87ba223e838d39e5ee66ebeea8b63e8a6bffb4a2b19f5b291e46d1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:6fb1a85021a8411e0470cca8a43d461db915d2df605657389c4f0595d2e42e91
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5548142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8780d448219e4996eb219326ba6943b7e05f04ab1189a6f1dcf2e013058e3e36`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:47:57 GMT
COPY file:33d3e4ce6e17dc907ca0b478996354d26d433431b7bf48ae5bef3ec2ea1359f1 in /nats-server 
# Wed, 13 Mar 2024 01:47:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:47:57 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:47:57 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:47:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce8539fabe7af34129953a073c64515d008d19eac52a820ef52368f6411e540d`  
		Last Modified: Wed, 13 Mar 2024 01:48:46 GMT  
		Size: 5.5 MB (5547633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5208dae10516783bd9b5be071d7f3d39c84e1138b3887856c85f570ec4f588c`  
		Last Modified: Wed, 13 Mar 2024 01:48:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:b717fb731a88e81bdabf9b7eb28e2ee0fa423ff801dcd5819fb4ffaf217cb208
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5263761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51552a7d22c2c5ca2447ff2b4198de16cfdff9a116a3c54ef5af0d997a9469f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:49:35 GMT
COPY file:c24c6855bab6e8b64a222738f44249dd58afe5ec56a34cfd64493e736f5325df in /nats-server 
# Wed, 13 Mar 2024 00:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:49:35 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:49:35 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:49:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bc2b5fa4421ea8f446fd52c0a8e7c8c6e048dc4aa6a096fb60765aa281147267`  
		Last Modified: Wed, 13 Mar 2024 00:50:20 GMT  
		Size: 5.3 MB (5263253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652cf78472b592b1ea355485d1a353340ba41c0d01b26f15ffacc090db84d7bb`  
		Last Modified: Wed, 13 Mar 2024 00:50:19 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:07d02d1f567ff67a36ece1f90364e466f099db860d2e8ec1f2143bec1c3710f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5956a4e3835d4532ea5cbfc23f7b2e2d96d15a877f42392feea63afa16be107b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:35:52 GMT
COPY file:6899efa16d7091375dc53de2fc1e5686e82569d9799d6cede2e40b0a8b6abb48 in /nats-server 
# Wed, 13 Mar 2024 00:35:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:35:52 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:35:52 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:35:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:68296288971fdb3ddfe9bfba9b6a79725a69e891fb82cd5708f088afaac9929f`  
		Last Modified: Wed, 13 Mar 2024 00:36:43 GMT  
		Size: 5.3 MB (5254529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652026202bce83174144280de06b0537518e9d13e1674ac88f0d7e8491a2e440`  
		Last Modified: Wed, 13 Mar 2024 00:36:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f8017338e2c0dd9d3adb17672dd8226d475d5c810fa5f742c27a1d77f6e0c0e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8216507954fc8ffbaa79f3aa0908756fb3b5e699a13215671cf23837d30ca343`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:40:40 GMT
COPY file:674069719b01a345db55aa1ea35485a8b6f0cf0eed465ae05a0c00073e2ab2ab in /nats-server 
# Wed, 13 Mar 2024 00:40:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:40:40 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:40:40 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:40:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d5466aeaf1139b432e415e6412234c167a91220e74d17f50be1a2de5b0fb1b21`  
		Last Modified: Wed, 13 Mar 2024 00:41:26 GMT  
		Size: 5.1 MB (5117178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562c0bd40d1b70ec911e4b7219f7867675e2ad1c67899a3643f13d261d792187`  
		Last Modified: Wed, 13 Mar 2024 00:41:25 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:e964ace9a5047268966aa2f1f2e10472325f21ac790016722c0a9090997a39f1
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a273f9d6d6aa560ff8df97aee7e4c13f87044f2be0081b07ba0f4a0fafd81a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 16 Feb 2024 19:24:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:29:00 GMT
COPY file:0e1c98477f605478a27423b67d1c7bf88d4b2a56d0696ea31430a8a59b294dd8 in /nats-server 
# Wed, 13 Mar 2024 01:29:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:29:01 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:29:01 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:29:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7eaf17599ba122502fe00d1cb4014722df0b46a83f614f9430f71b816a6999f8`  
		Last Modified: Wed, 13 Mar 2024 01:29:44 GMT  
		Size: 5.1 MB (5096748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b8d7d148d9f2f60c0b13204daf3a2f76ff85991d79fe4fd82aa842a3d77a1d`  
		Last Modified: Wed, 13 Mar 2024 01:29:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:21d23f9777f88070c60ce8bf669dd9169ad10d91ddae1f43c02b5419cc5fcbc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5430830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a9daecac5ba461be180b94ca61fe053ebe1e5c23af8e61522f1854982e6157`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:15:09 GMT
COPY file:cc94c349de0e266f428d63773845fb669334304c5fbcffeec57553d333126f22 in /nats-server 
# Wed, 13 Mar 2024 01:15:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:15:09 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:15:09 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:15:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0bf838b872f1e012c580bbff8d1e66a09a7b05a85651db222851ea3323dab3d2`  
		Last Modified: Wed, 13 Mar 2024 01:16:47 GMT  
		Size: 5.4 MB (5430321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668de88817078f4ef2cf284dff428f40567f94b7132efee56fe3abe6264e6d42`  
		Last Modified: Wed, 13 Mar 2024 01:16:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:d7d19aca6454b871d5135f9cc685694349f0f72c02f00641f749e391f828e8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats@sha256:7fa1366a0cee4e50f2a2402c01dd3ea274be364140f556693350356d0e2db63c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2131507333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3743311440c84bac2fc9c9e5e74770053c07f4480d2901f7abe6813c87cf4dae`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 02:18:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Mar 2024 02:18:28 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:18:29 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 02:18:30 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.12/nats-server-v2.10.12-windows-amd64.zip
# Wed, 13 Mar 2024 02:18:30 GMT
ENV NATS_SERVER_SHASUM=bc944f832fdc3eaa0072c0a5e278efd672cec394159661070e7aea4f5d483cbc
# Wed, 13 Mar 2024 02:19:47 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Mar 2024 02:21:44 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 13 Mar 2024 02:21:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Mar 2024 02:21:45 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 02:21:46 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Mar 2024 02:21:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e169e85f3c664d99b16235c550eb744e7e1421ceb3b4a239fd727321ccddc77`  
		Last Modified: Wed, 13 Mar 2024 02:26:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7cb8b6faf23b1820a39bd95d7664a27dd6143342b384e0331e51b7e7ba82b72`  
		Last Modified: Wed, 13 Mar 2024 02:26:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3886c92295e481a562d7a5fe9418c1de632210a05c19f06705629bc95800902`  
		Last Modified: Wed, 13 Mar 2024 02:26:10 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b851f5dbeec69a3c0b7cef01f0be439c3febe18363296e9980de2f7ba04d04ec`  
		Last Modified: Wed, 13 Mar 2024 02:26:10 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ac0c5c4d4063f650788f99bee2df77584d4cce33709529fbf1c1287c77e6b1`  
		Last Modified: Wed, 13 Mar 2024 02:26:10 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce303014e2084243978d691011a901e05e79a3dd3aca02f6bf15b0111f313ba`  
		Last Modified: Wed, 13 Mar 2024 02:26:10 GMT  
		Size: 445.8 KB (445828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209561aab82234ce8e269b77a1c45eb4d10f5c3d9ec877e078db4d5b72ab672c`  
		Last Modified: Wed, 13 Mar 2024 02:26:09 GMT  
		Size: 5.9 MB (5948270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b859631a59ecabb2bf06bbe8d86a2994232ad2d5852842b40363bf2bbb528cc7`  
		Last Modified: Wed, 13 Mar 2024 02:26:08 GMT  
		Size: 2.0 KB (1985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b5005070ee0dabaf577a0f2e898332aab7a1ec26da577b3d2ceb9ffeaaf343`  
		Last Modified: Wed, 13 Mar 2024 02:26:08 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4db2f7ed46b07e7feccb03f8e63ad91142de5165acf6c898a5aac89b0cd559`  
		Last Modified: Wed, 13 Mar 2024 02:26:08 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81813a03072d63cfbad1f640180a29dfc80c337f2a4ffeaeb116769574cda27`  
		Last Modified: Wed, 13 Mar 2024 02:26:08 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:d7d19aca6454b871d5135f9cc685694349f0f72c02f00641f749e391f828e8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats@sha256:7fa1366a0cee4e50f2a2402c01dd3ea274be364140f556693350356d0e2db63c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2131507333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3743311440c84bac2fc9c9e5e74770053c07f4480d2901f7abe6813c87cf4dae`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 02:18:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Mar 2024 02:18:28 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:18:29 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 02:18:30 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.12/nats-server-v2.10.12-windows-amd64.zip
# Wed, 13 Mar 2024 02:18:30 GMT
ENV NATS_SERVER_SHASUM=bc944f832fdc3eaa0072c0a5e278efd672cec394159661070e7aea4f5d483cbc
# Wed, 13 Mar 2024 02:19:47 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Mar 2024 02:21:44 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 13 Mar 2024 02:21:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Mar 2024 02:21:45 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 02:21:46 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Mar 2024 02:21:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e169e85f3c664d99b16235c550eb744e7e1421ceb3b4a239fd727321ccddc77`  
		Last Modified: Wed, 13 Mar 2024 02:26:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7cb8b6faf23b1820a39bd95d7664a27dd6143342b384e0331e51b7e7ba82b72`  
		Last Modified: Wed, 13 Mar 2024 02:26:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3886c92295e481a562d7a5fe9418c1de632210a05c19f06705629bc95800902`  
		Last Modified: Wed, 13 Mar 2024 02:26:10 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b851f5dbeec69a3c0b7cef01f0be439c3febe18363296e9980de2f7ba04d04ec`  
		Last Modified: Wed, 13 Mar 2024 02:26:10 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ac0c5c4d4063f650788f99bee2df77584d4cce33709529fbf1c1287c77e6b1`  
		Last Modified: Wed, 13 Mar 2024 02:26:10 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce303014e2084243978d691011a901e05e79a3dd3aca02f6bf15b0111f313ba`  
		Last Modified: Wed, 13 Mar 2024 02:26:10 GMT  
		Size: 445.8 KB (445828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209561aab82234ce8e269b77a1c45eb4d10f5c3d9ec877e078db4d5b72ab672c`  
		Last Modified: Wed, 13 Mar 2024 02:26:09 GMT  
		Size: 5.9 MB (5948270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b859631a59ecabb2bf06bbe8d86a2994232ad2d5852842b40363bf2bbb528cc7`  
		Last Modified: Wed, 13 Mar 2024 02:26:08 GMT  
		Size: 2.0 KB (1985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b5005070ee0dabaf577a0f2e898332aab7a1ec26da577b3d2ceb9ffeaaf343`  
		Last Modified: Wed, 13 Mar 2024 02:26:08 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4db2f7ed46b07e7feccb03f8e63ad91142de5165acf6c898a5aac89b0cd559`  
		Last Modified: Wed, 13 Mar 2024 02:26:08 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81813a03072d63cfbad1f640180a29dfc80c337f2a4ffeaeb116769574cda27`  
		Last Modified: Wed, 13 Mar 2024 02:26:08 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:9b1ee0caf5737f6b44b15da670b866900af4077d6ae6e2a170466e2e0fc68cb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5576; amd64

### `nats:2.10` - linux; amd64

```console
$ docker pull nats@sha256:6fb1a85021a8411e0470cca8a43d461db915d2df605657389c4f0595d2e42e91
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5548142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8780d448219e4996eb219326ba6943b7e05f04ab1189a6f1dcf2e013058e3e36`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:47:57 GMT
COPY file:33d3e4ce6e17dc907ca0b478996354d26d433431b7bf48ae5bef3ec2ea1359f1 in /nats-server 
# Wed, 13 Mar 2024 01:47:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:47:57 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:47:57 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:47:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce8539fabe7af34129953a073c64515d008d19eac52a820ef52368f6411e540d`  
		Last Modified: Wed, 13 Mar 2024 01:48:46 GMT  
		Size: 5.5 MB (5547633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5208dae10516783bd9b5be071d7f3d39c84e1138b3887856c85f570ec4f588c`  
		Last Modified: Wed, 13 Mar 2024 01:48:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:b717fb731a88e81bdabf9b7eb28e2ee0fa423ff801dcd5819fb4ffaf217cb208
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5263761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51552a7d22c2c5ca2447ff2b4198de16cfdff9a116a3c54ef5af0d997a9469f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:49:35 GMT
COPY file:c24c6855bab6e8b64a222738f44249dd58afe5ec56a34cfd64493e736f5325df in /nats-server 
# Wed, 13 Mar 2024 00:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:49:35 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:49:35 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:49:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bc2b5fa4421ea8f446fd52c0a8e7c8c6e048dc4aa6a096fb60765aa281147267`  
		Last Modified: Wed, 13 Mar 2024 00:50:20 GMT  
		Size: 5.3 MB (5263253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652cf78472b592b1ea355485d1a353340ba41c0d01b26f15ffacc090db84d7bb`  
		Last Modified: Wed, 13 Mar 2024 00:50:19 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:07d02d1f567ff67a36ece1f90364e466f099db860d2e8ec1f2143bec1c3710f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5956a4e3835d4532ea5cbfc23f7b2e2d96d15a877f42392feea63afa16be107b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:35:52 GMT
COPY file:6899efa16d7091375dc53de2fc1e5686e82569d9799d6cede2e40b0a8b6abb48 in /nats-server 
# Wed, 13 Mar 2024 00:35:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:35:52 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:35:52 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:35:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:68296288971fdb3ddfe9bfba9b6a79725a69e891fb82cd5708f088afaac9929f`  
		Last Modified: Wed, 13 Mar 2024 00:36:43 GMT  
		Size: 5.3 MB (5254529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652026202bce83174144280de06b0537518e9d13e1674ac88f0d7e8491a2e440`  
		Last Modified: Wed, 13 Mar 2024 00:36:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f8017338e2c0dd9d3adb17672dd8226d475d5c810fa5f742c27a1d77f6e0c0e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8216507954fc8ffbaa79f3aa0908756fb3b5e699a13215671cf23837d30ca343`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:40:40 GMT
COPY file:674069719b01a345db55aa1ea35485a8b6f0cf0eed465ae05a0c00073e2ab2ab in /nats-server 
# Wed, 13 Mar 2024 00:40:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:40:40 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:40:40 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:40:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d5466aeaf1139b432e415e6412234c167a91220e74d17f50be1a2de5b0fb1b21`  
		Last Modified: Wed, 13 Mar 2024 00:41:26 GMT  
		Size: 5.1 MB (5117178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562c0bd40d1b70ec911e4b7219f7867675e2ad1c67899a3643f13d261d792187`  
		Last Modified: Wed, 13 Mar 2024 00:41:25 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; ppc64le

```console
$ docker pull nats@sha256:e964ace9a5047268966aa2f1f2e10472325f21ac790016722c0a9090997a39f1
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a273f9d6d6aa560ff8df97aee7e4c13f87044f2be0081b07ba0f4a0fafd81a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 16 Feb 2024 19:24:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:29:00 GMT
COPY file:0e1c98477f605478a27423b67d1c7bf88d4b2a56d0696ea31430a8a59b294dd8 in /nats-server 
# Wed, 13 Mar 2024 01:29:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:29:01 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:29:01 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:29:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7eaf17599ba122502fe00d1cb4014722df0b46a83f614f9430f71b816a6999f8`  
		Last Modified: Wed, 13 Mar 2024 01:29:44 GMT  
		Size: 5.1 MB (5096748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b8d7d148d9f2f60c0b13204daf3a2f76ff85991d79fe4fd82aa842a3d77a1d`  
		Last Modified: Wed, 13 Mar 2024 01:29:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; s390x

```console
$ docker pull nats@sha256:21d23f9777f88070c60ce8bf669dd9169ad10d91ddae1f43c02b5419cc5fcbc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5430830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a9daecac5ba461be180b94ca61fe053ebe1e5c23af8e61522f1854982e6157`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:15:09 GMT
COPY file:cc94c349de0e266f428d63773845fb669334304c5fbcffeec57553d333126f22 in /nats-server 
# Wed, 13 Mar 2024 01:15:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:15:09 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:15:09 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:15:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0bf838b872f1e012c580bbff8d1e66a09a7b05a85651db222851ea3323dab3d2`  
		Last Modified: Wed, 13 Mar 2024 01:16:47 GMT  
		Size: 5.4 MB (5430321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668de88817078f4ef2cf284dff428f40567f94b7132efee56fe3abe6264e6d42`  
		Last Modified: Wed, 13 Mar 2024 01:16:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats@sha256:1bb4572909b97a5aea3e76230e9d09a1078a21d41ba7000bd5afbe5225fc1568
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110290182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a1f3d16c6f5aea885d55ec76e40c984ca8763448ae4b9b424ec4d5bec24fc8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 02:21:55 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:21:57 GMT
RUN cmd /S /C #(nop) COPY file:b8b09037eca4c9daccbaf940396fb084777535cdce4ec562f44c0b727cf16e3e in C:\nats-server.exe 
# Wed, 13 Mar 2024 02:21:57 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Mar 2024 02:21:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 02:21:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Mar 2024 02:21:59 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e772fbc90f54f9eab2951a9615b88e9eca8fc78909aba2cb3678cc214eb88ae2`  
		Last Modified: Wed, 13 Mar 2024 02:26:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9cd82df1e1baf71960c98c3ca3996de090e25ce522c16d07628ea7705a1c7b`  
		Last Modified: Wed, 13 Mar 2024 02:26:26 GMT  
		Size: 5.7 MB (5663658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce47417df81557c57ff79790516751ae140155b5d06e2f8538fcf4d7e94a1004`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c07d5748899da1f68ed98e7331fa02c4175552921ad31f2ec6ba40f208c69d`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89220da9dce87f2d7ea149e170563fa7bac7ae732a1b8c89f51d60e5da18020e`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78635ce16de8337563a88c3a78835fed97c207dc9254d2dc0d06594b9926b0e0`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:7a3dedb2152d01809b0343a8fce27241d6eae68f65200a8e6da78d88ac4257a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10-alpine` - linux; amd64

```console
$ docker pull nats@sha256:04333a656bd283d8642c365f790bbd26a0dd2919a0d29dd75998776c6ef7207d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9577940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606a0820025fa72d87e550430e7c14c89557b69fecac16e732dbf2d3c0bcaa76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 01:47:48 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 01:47:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 01:47:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 01:47:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 01:47:51 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:47:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 01:47:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a35673fda7fb893fc2c187357a17a1c13cb7b1958fa8d97eee3155901c44fba`  
		Last Modified: Wed, 13 Mar 2024 01:48:27 GMT  
		Size: 6.2 MB (6168214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdf5efdff66ae170a3b780d793b6b5d821138b53926474870aebccb2af5ee57`  
		Last Modified: Wed, 13 Mar 2024 01:48:25 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c95813002da682382a4ba34c5210071c10314593a044ab5120d5d8780b07e4a`  
		Last Modified: Wed, 13 Mar 2024 01:48:25 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:6e93abf037354dbe3af08ece7d516f8a4e61c675fbab84594adf10b108082777
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9051274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075217343e913477fcd44713b6ae36fa6c55e5a333eca26c9e952a97e51a14f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 00:49:24 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 00:49:28 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 00:49:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 00:49:28 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 00:49:28 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:49:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 00:49:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b7bd072e2424f96ed51dee5137cd95e43686fc4624f2d2feee365fd304f5fc`  
		Last Modified: Wed, 13 Mar 2024 00:50:00 GMT  
		Size: 5.9 MB (5884880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cd491dd798da6f6a27555feb3be80ea1e29262571e10acde00300ee332740f`  
		Last Modified: Wed, 13 Mar 2024 00:49:59 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568e37ef91f5962c31828a2adc1588dcec32dbe5859699372ff1656c5659a915`  
		Last Modified: Wed, 13 Mar 2024 00:49:59 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:06913e056cdc6c1997068e0fe2e6355f571c04f12afd48f9e02cea1f16554016
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8795654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fbc0f10b6a6c92c2a77318fa3a4f9b73f5dc9a8e0304b5475f614294196d6d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 00:35:35 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 00:35:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 00:35:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 00:35:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 00:35:39 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:35:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 00:35:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55a741d01acaf5448cb8ffa39243f9f34261fd88e914772554124224189cc81`  
		Last Modified: Wed, 13 Mar 2024 00:36:23 GMT  
		Size: 5.9 MB (5875752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d61266118e4acdda142cd2ac76a4ef35e24e7502ec60b4cf26cf49a145acdc`  
		Last Modified: Wed, 13 Mar 2024 00:36:18 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1e59e375c0cd803e4186b41a2566a69e1f0a8b88ba1cf0954a5a00d33af0d2`  
		Last Modified: Wed, 13 Mar 2024 00:36:18 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:62b700c1d94d9c9164795d902681026f20a4c2c215e70dea7661f632c43f93b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9088728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b8a7d9375b33a34c6019c8a05fc253872624aaba1066208fa1ae728471c370`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 00:40:21 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 00:40:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 00:40:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 00:40:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 00:40:24 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:40:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 00:40:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46909e9837d35c1cb85abbf0a81ed8df7ac00f9ac7df67d275bd7edb87fdc88b`  
		Last Modified: Wed, 13 Mar 2024 00:41:06 GMT  
		Size: 5.7 MB (5740016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a74044cf86ca3325a7a324fbd7d08694e721bad44f2f7865d35ed3b3ce23b4`  
		Last Modified: Wed, 13 Mar 2024 00:41:05 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f776b77a6001c5e0fd42db5610aa2acfeecb867c59a3559a2cd6983a5067ad6c`  
		Last Modified: Wed, 13 Mar 2024 00:41:05 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:e73b5c826fe9e8fc554f8e4440d8ae0504b4f7899d6c5bc38c6b68a0d9e705d0
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9078995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96541c86763ab33908efa9617f909b1b23853fc66f5740829aaa97d4fb819d4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 01:28:25 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 01:28:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 01:28:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 01:28:31 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 01:28:32 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:28:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 01:28:33 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd4d0c36112be2592baa66fdba8327cff756029be8e96f803015fce9a8bfab7`  
		Last Modified: Wed, 13 Mar 2024 01:29:22 GMT  
		Size: 5.7 MB (5719643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217c8e169d797596a8b822f912ec2ba564e491f6949ecd95a5a405d275c5a5a6`  
		Last Modified: Wed, 13 Mar 2024 01:29:21 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad20a946927156b80304d831d9d123a0ba902501570002869968e92231bbd32`  
		Last Modified: Wed, 13 Mar 2024 01:29:21 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; s390x

```console
$ docker pull nats@sha256:49f1c4fa564a8f8073315103db29d373273c7e703c43d6f275a1acc3ab010a3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9296162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7420d0049b07e2c363f050c33e0ac3ba0fe39fe6d0bee0ffea5c71f2fdf0749`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 01:14:00 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 01:14:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 01:14:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 01:14:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 01:14:03 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:14:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 01:14:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d4a8da7be6313cc596f154b85b638749ab970144f58575af5bef288a9e44ce`  
		Last Modified: Wed, 13 Mar 2024 01:16:34 GMT  
		Size: 6.1 MB (6052529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c87220ce1b5f8a7ed2e5ab6caf39ac9028ba6d25133711633f25a21b60c4b24`  
		Last Modified: Wed, 13 Mar 2024 01:16:33 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43f30dc994a90cc1c2a38e8a5176d279817dd3d25ffe3d8ac67b665c606f3b3`  
		Last Modified: Wed, 13 Mar 2024 01:16:33 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine3.19`

```console
$ docker pull nats@sha256:7a3dedb2152d01809b0343a8fce27241d6eae68f65200a8e6da78d88ac4257a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10-alpine3.19` - linux; amd64

```console
$ docker pull nats@sha256:04333a656bd283d8642c365f790bbd26a0dd2919a0d29dd75998776c6ef7207d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9577940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606a0820025fa72d87e550430e7c14c89557b69fecac16e732dbf2d3c0bcaa76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 01:47:48 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 01:47:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 01:47:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 01:47:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 01:47:51 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:47:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 01:47:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a35673fda7fb893fc2c187357a17a1c13cb7b1958fa8d97eee3155901c44fba`  
		Last Modified: Wed, 13 Mar 2024 01:48:27 GMT  
		Size: 6.2 MB (6168214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdf5efdff66ae170a3b780d793b6b5d821138b53926474870aebccb2af5ee57`  
		Last Modified: Wed, 13 Mar 2024 01:48:25 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c95813002da682382a4ba34c5210071c10314593a044ab5120d5d8780b07e4a`  
		Last Modified: Wed, 13 Mar 2024 01:48:25 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; arm variant v6

```console
$ docker pull nats@sha256:6e93abf037354dbe3af08ece7d516f8a4e61c675fbab84594adf10b108082777
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9051274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075217343e913477fcd44713b6ae36fa6c55e5a333eca26c9e952a97e51a14f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 00:49:24 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 00:49:28 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 00:49:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 00:49:28 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 00:49:28 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:49:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 00:49:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b7bd072e2424f96ed51dee5137cd95e43686fc4624f2d2feee365fd304f5fc`  
		Last Modified: Wed, 13 Mar 2024 00:50:00 GMT  
		Size: 5.9 MB (5884880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cd491dd798da6f6a27555feb3be80ea1e29262571e10acde00300ee332740f`  
		Last Modified: Wed, 13 Mar 2024 00:49:59 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568e37ef91f5962c31828a2adc1588dcec32dbe5859699372ff1656c5659a915`  
		Last Modified: Wed, 13 Mar 2024 00:49:59 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:06913e056cdc6c1997068e0fe2e6355f571c04f12afd48f9e02cea1f16554016
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8795654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fbc0f10b6a6c92c2a77318fa3a4f9b73f5dc9a8e0304b5475f614294196d6d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 00:35:35 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 00:35:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 00:35:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 00:35:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 00:35:39 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:35:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 00:35:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55a741d01acaf5448cb8ffa39243f9f34261fd88e914772554124224189cc81`  
		Last Modified: Wed, 13 Mar 2024 00:36:23 GMT  
		Size: 5.9 MB (5875752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d61266118e4acdda142cd2ac76a4ef35e24e7502ec60b4cf26cf49a145acdc`  
		Last Modified: Wed, 13 Mar 2024 00:36:18 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1e59e375c0cd803e4186b41a2566a69e1f0a8b88ba1cf0954a5a00d33af0d2`  
		Last Modified: Wed, 13 Mar 2024 00:36:18 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:62b700c1d94d9c9164795d902681026f20a4c2c215e70dea7661f632c43f93b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9088728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b8a7d9375b33a34c6019c8a05fc253872624aaba1066208fa1ae728471c370`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 00:40:21 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 00:40:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 00:40:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 00:40:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 00:40:24 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:40:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 00:40:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46909e9837d35c1cb85abbf0a81ed8df7ac00f9ac7df67d275bd7edb87fdc88b`  
		Last Modified: Wed, 13 Mar 2024 00:41:06 GMT  
		Size: 5.7 MB (5740016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a74044cf86ca3325a7a324fbd7d08694e721bad44f2f7865d35ed3b3ce23b4`  
		Last Modified: Wed, 13 Mar 2024 00:41:05 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f776b77a6001c5e0fd42db5610aa2acfeecb867c59a3559a2cd6983a5067ad6c`  
		Last Modified: Wed, 13 Mar 2024 00:41:05 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; ppc64le

```console
$ docker pull nats@sha256:e73b5c826fe9e8fc554f8e4440d8ae0504b4f7899d6c5bc38c6b68a0d9e705d0
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9078995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96541c86763ab33908efa9617f909b1b23853fc66f5740829aaa97d4fb819d4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 01:28:25 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 01:28:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 01:28:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 01:28:31 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 01:28:32 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:28:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 01:28:33 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd4d0c36112be2592baa66fdba8327cff756029be8e96f803015fce9a8bfab7`  
		Last Modified: Wed, 13 Mar 2024 01:29:22 GMT  
		Size: 5.7 MB (5719643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217c8e169d797596a8b822f912ec2ba564e491f6949ecd95a5a405d275c5a5a6`  
		Last Modified: Wed, 13 Mar 2024 01:29:21 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad20a946927156b80304d831d9d123a0ba902501570002869968e92231bbd32`  
		Last Modified: Wed, 13 Mar 2024 01:29:21 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; s390x

```console
$ docker pull nats@sha256:49f1c4fa564a8f8073315103db29d373273c7e703c43d6f275a1acc3ab010a3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9296162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7420d0049b07e2c363f050c33e0ac3ba0fe39fe6d0bee0ffea5c71f2fdf0749`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 01:14:00 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 01:14:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 01:14:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 01:14:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 01:14:03 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:14:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 01:14:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d4a8da7be6313cc596f154b85b638749ab970144f58575af5bef288a9e44ce`  
		Last Modified: Wed, 13 Mar 2024 01:16:34 GMT  
		Size: 6.1 MB (6052529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c87220ce1b5f8a7ed2e5ab6caf39ac9028ba6d25133711633f25a21b60c4b24`  
		Last Modified: Wed, 13 Mar 2024 01:16:33 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43f30dc994a90cc1c2a38e8a5176d279817dd3d25ffe3d8ac67b665c606f3b3`  
		Last Modified: Wed, 13 Mar 2024 01:16:33 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:bb90d21b87ba223e838d39e5ee66ebeea8b63e8a6bffb4a2b19f5b291e46d1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10-linux` - linux; amd64

```console
$ docker pull nats@sha256:6fb1a85021a8411e0470cca8a43d461db915d2df605657389c4f0595d2e42e91
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5548142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8780d448219e4996eb219326ba6943b7e05f04ab1189a6f1dcf2e013058e3e36`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:47:57 GMT
COPY file:33d3e4ce6e17dc907ca0b478996354d26d433431b7bf48ae5bef3ec2ea1359f1 in /nats-server 
# Wed, 13 Mar 2024 01:47:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:47:57 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:47:57 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:47:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce8539fabe7af34129953a073c64515d008d19eac52a820ef52368f6411e540d`  
		Last Modified: Wed, 13 Mar 2024 01:48:46 GMT  
		Size: 5.5 MB (5547633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5208dae10516783bd9b5be071d7f3d39c84e1138b3887856c85f570ec4f588c`  
		Last Modified: Wed, 13 Mar 2024 01:48:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:b717fb731a88e81bdabf9b7eb28e2ee0fa423ff801dcd5819fb4ffaf217cb208
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5263761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51552a7d22c2c5ca2447ff2b4198de16cfdff9a116a3c54ef5af0d997a9469f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:49:35 GMT
COPY file:c24c6855bab6e8b64a222738f44249dd58afe5ec56a34cfd64493e736f5325df in /nats-server 
# Wed, 13 Mar 2024 00:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:49:35 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:49:35 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:49:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bc2b5fa4421ea8f446fd52c0a8e7c8c6e048dc4aa6a096fb60765aa281147267`  
		Last Modified: Wed, 13 Mar 2024 00:50:20 GMT  
		Size: 5.3 MB (5263253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652cf78472b592b1ea355485d1a353340ba41c0d01b26f15ffacc090db84d7bb`  
		Last Modified: Wed, 13 Mar 2024 00:50:19 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:07d02d1f567ff67a36ece1f90364e466f099db860d2e8ec1f2143bec1c3710f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5956a4e3835d4532ea5cbfc23f7b2e2d96d15a877f42392feea63afa16be107b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:35:52 GMT
COPY file:6899efa16d7091375dc53de2fc1e5686e82569d9799d6cede2e40b0a8b6abb48 in /nats-server 
# Wed, 13 Mar 2024 00:35:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:35:52 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:35:52 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:35:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:68296288971fdb3ddfe9bfba9b6a79725a69e891fb82cd5708f088afaac9929f`  
		Last Modified: Wed, 13 Mar 2024 00:36:43 GMT  
		Size: 5.3 MB (5254529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652026202bce83174144280de06b0537518e9d13e1674ac88f0d7e8491a2e440`  
		Last Modified: Wed, 13 Mar 2024 00:36:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f8017338e2c0dd9d3adb17672dd8226d475d5c810fa5f742c27a1d77f6e0c0e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8216507954fc8ffbaa79f3aa0908756fb3b5e699a13215671cf23837d30ca343`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:40:40 GMT
COPY file:674069719b01a345db55aa1ea35485a8b6f0cf0eed465ae05a0c00073e2ab2ab in /nats-server 
# Wed, 13 Mar 2024 00:40:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:40:40 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:40:40 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:40:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d5466aeaf1139b432e415e6412234c167a91220e74d17f50be1a2de5b0fb1b21`  
		Last Modified: Wed, 13 Mar 2024 00:41:26 GMT  
		Size: 5.1 MB (5117178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562c0bd40d1b70ec911e4b7219f7867675e2ad1c67899a3643f13d261d792187`  
		Last Modified: Wed, 13 Mar 2024 00:41:25 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:e964ace9a5047268966aa2f1f2e10472325f21ac790016722c0a9090997a39f1
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a273f9d6d6aa560ff8df97aee7e4c13f87044f2be0081b07ba0f4a0fafd81a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 16 Feb 2024 19:24:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:29:00 GMT
COPY file:0e1c98477f605478a27423b67d1c7bf88d4b2a56d0696ea31430a8a59b294dd8 in /nats-server 
# Wed, 13 Mar 2024 01:29:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:29:01 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:29:01 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:29:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7eaf17599ba122502fe00d1cb4014722df0b46a83f614f9430f71b816a6999f8`  
		Last Modified: Wed, 13 Mar 2024 01:29:44 GMT  
		Size: 5.1 MB (5096748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b8d7d148d9f2f60c0b13204daf3a2f76ff85991d79fe4fd82aa842a3d77a1d`  
		Last Modified: Wed, 13 Mar 2024 01:29:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; s390x

```console
$ docker pull nats@sha256:21d23f9777f88070c60ce8bf669dd9169ad10d91ddae1f43c02b5419cc5fcbc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5430830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a9daecac5ba461be180b94ca61fe053ebe1e5c23af8e61522f1854982e6157`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:15:09 GMT
COPY file:cc94c349de0e266f428d63773845fb669334304c5fbcffeec57553d333126f22 in /nats-server 
# Wed, 13 Mar 2024 01:15:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:15:09 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:15:09 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:15:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0bf838b872f1e012c580bbff8d1e66a09a7b05a85651db222851ea3323dab3d2`  
		Last Modified: Wed, 13 Mar 2024 01:16:47 GMT  
		Size: 5.4 MB (5430321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668de88817078f4ef2cf284dff428f40567f94b7132efee56fe3abe6264e6d42`  
		Last Modified: Wed, 13 Mar 2024 01:16:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver`

```console
$ docker pull nats@sha256:38b381e6f2834d3c5120087f02c9d13f238a2142f54568a208fa74d554bb62d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats:2.10-nanoserver` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats@sha256:1bb4572909b97a5aea3e76230e9d09a1078a21d41ba7000bd5afbe5225fc1568
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110290182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a1f3d16c6f5aea885d55ec76e40c984ca8763448ae4b9b424ec4d5bec24fc8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 02:21:55 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:21:57 GMT
RUN cmd /S /C #(nop) COPY file:b8b09037eca4c9daccbaf940396fb084777535cdce4ec562f44c0b727cf16e3e in C:\nats-server.exe 
# Wed, 13 Mar 2024 02:21:57 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Mar 2024 02:21:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 02:21:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Mar 2024 02:21:59 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e772fbc90f54f9eab2951a9615b88e9eca8fc78909aba2cb3678cc214eb88ae2`  
		Last Modified: Wed, 13 Mar 2024 02:26:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9cd82df1e1baf71960c98c3ca3996de090e25ce522c16d07628ea7705a1c7b`  
		Last Modified: Wed, 13 Mar 2024 02:26:26 GMT  
		Size: 5.7 MB (5663658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce47417df81557c57ff79790516751ae140155b5d06e2f8538fcf4d7e94a1004`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c07d5748899da1f68ed98e7331fa02c4175552921ad31f2ec6ba40f208c69d`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89220da9dce87f2d7ea149e170563fa7bac7ae732a1b8c89f51d60e5da18020e`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78635ce16de8337563a88c3a78835fed97c207dc9254d2dc0d06594b9926b0e0`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-1809`

```console
$ docker pull nats@sha256:38b381e6f2834d3c5120087f02c9d13f238a2142f54568a208fa74d554bb62d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats:2.10-nanoserver-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats@sha256:1bb4572909b97a5aea3e76230e9d09a1078a21d41ba7000bd5afbe5225fc1568
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110290182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a1f3d16c6f5aea885d55ec76e40c984ca8763448ae4b9b424ec4d5bec24fc8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 02:21:55 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:21:57 GMT
RUN cmd /S /C #(nop) COPY file:b8b09037eca4c9daccbaf940396fb084777535cdce4ec562f44c0b727cf16e3e in C:\nats-server.exe 
# Wed, 13 Mar 2024 02:21:57 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Mar 2024 02:21:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 02:21:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Mar 2024 02:21:59 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e772fbc90f54f9eab2951a9615b88e9eca8fc78909aba2cb3678cc214eb88ae2`  
		Last Modified: Wed, 13 Mar 2024 02:26:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9cd82df1e1baf71960c98c3ca3996de090e25ce522c16d07628ea7705a1c7b`  
		Last Modified: Wed, 13 Mar 2024 02:26:26 GMT  
		Size: 5.7 MB (5663658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce47417df81557c57ff79790516751ae140155b5d06e2f8538fcf4d7e94a1004`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c07d5748899da1f68ed98e7331fa02c4175552921ad31f2ec6ba40f208c69d`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89220da9dce87f2d7ea149e170563fa7bac7ae732a1b8c89f51d60e5da18020e`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78635ce16de8337563a88c3a78835fed97c207dc9254d2dc0d06594b9926b0e0`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-scratch`

```console
$ docker pull nats@sha256:bb90d21b87ba223e838d39e5ee66ebeea8b63e8a6bffb4a2b19f5b291e46d1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10-scratch` - linux; amd64

```console
$ docker pull nats@sha256:6fb1a85021a8411e0470cca8a43d461db915d2df605657389c4f0595d2e42e91
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5548142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8780d448219e4996eb219326ba6943b7e05f04ab1189a6f1dcf2e013058e3e36`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:47:57 GMT
COPY file:33d3e4ce6e17dc907ca0b478996354d26d433431b7bf48ae5bef3ec2ea1359f1 in /nats-server 
# Wed, 13 Mar 2024 01:47:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:47:57 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:47:57 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:47:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce8539fabe7af34129953a073c64515d008d19eac52a820ef52368f6411e540d`  
		Last Modified: Wed, 13 Mar 2024 01:48:46 GMT  
		Size: 5.5 MB (5547633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5208dae10516783bd9b5be071d7f3d39c84e1138b3887856c85f570ec4f588c`  
		Last Modified: Wed, 13 Mar 2024 01:48:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:b717fb731a88e81bdabf9b7eb28e2ee0fa423ff801dcd5819fb4ffaf217cb208
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5263761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51552a7d22c2c5ca2447ff2b4198de16cfdff9a116a3c54ef5af0d997a9469f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:49:35 GMT
COPY file:c24c6855bab6e8b64a222738f44249dd58afe5ec56a34cfd64493e736f5325df in /nats-server 
# Wed, 13 Mar 2024 00:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:49:35 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:49:35 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:49:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bc2b5fa4421ea8f446fd52c0a8e7c8c6e048dc4aa6a096fb60765aa281147267`  
		Last Modified: Wed, 13 Mar 2024 00:50:20 GMT  
		Size: 5.3 MB (5263253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652cf78472b592b1ea355485d1a353340ba41c0d01b26f15ffacc090db84d7bb`  
		Last Modified: Wed, 13 Mar 2024 00:50:19 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:07d02d1f567ff67a36ece1f90364e466f099db860d2e8ec1f2143bec1c3710f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5956a4e3835d4532ea5cbfc23f7b2e2d96d15a877f42392feea63afa16be107b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:35:52 GMT
COPY file:6899efa16d7091375dc53de2fc1e5686e82569d9799d6cede2e40b0a8b6abb48 in /nats-server 
# Wed, 13 Mar 2024 00:35:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:35:52 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:35:52 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:35:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:68296288971fdb3ddfe9bfba9b6a79725a69e891fb82cd5708f088afaac9929f`  
		Last Modified: Wed, 13 Mar 2024 00:36:43 GMT  
		Size: 5.3 MB (5254529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652026202bce83174144280de06b0537518e9d13e1674ac88f0d7e8491a2e440`  
		Last Modified: Wed, 13 Mar 2024 00:36:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f8017338e2c0dd9d3adb17672dd8226d475d5c810fa5f742c27a1d77f6e0c0e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8216507954fc8ffbaa79f3aa0908756fb3b5e699a13215671cf23837d30ca343`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:40:40 GMT
COPY file:674069719b01a345db55aa1ea35485a8b6f0cf0eed465ae05a0c00073e2ab2ab in /nats-server 
# Wed, 13 Mar 2024 00:40:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:40:40 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:40:40 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:40:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d5466aeaf1139b432e415e6412234c167a91220e74d17f50be1a2de5b0fb1b21`  
		Last Modified: Wed, 13 Mar 2024 00:41:26 GMT  
		Size: 5.1 MB (5117178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562c0bd40d1b70ec911e4b7219f7867675e2ad1c67899a3643f13d261d792187`  
		Last Modified: Wed, 13 Mar 2024 00:41:25 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:e964ace9a5047268966aa2f1f2e10472325f21ac790016722c0a9090997a39f1
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a273f9d6d6aa560ff8df97aee7e4c13f87044f2be0081b07ba0f4a0fafd81a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 16 Feb 2024 19:24:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:29:00 GMT
COPY file:0e1c98477f605478a27423b67d1c7bf88d4b2a56d0696ea31430a8a59b294dd8 in /nats-server 
# Wed, 13 Mar 2024 01:29:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:29:01 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:29:01 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:29:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7eaf17599ba122502fe00d1cb4014722df0b46a83f614f9430f71b816a6999f8`  
		Last Modified: Wed, 13 Mar 2024 01:29:44 GMT  
		Size: 5.1 MB (5096748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b8d7d148d9f2f60c0b13204daf3a2f76ff85991d79fe4fd82aa842a3d77a1d`  
		Last Modified: Wed, 13 Mar 2024 01:29:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; s390x

```console
$ docker pull nats@sha256:21d23f9777f88070c60ce8bf669dd9169ad10d91ddae1f43c02b5419cc5fcbc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5430830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a9daecac5ba461be180b94ca61fe053ebe1e5c23af8e61522f1854982e6157`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:15:09 GMT
COPY file:cc94c349de0e266f428d63773845fb669334304c5fbcffeec57553d333126f22 in /nats-server 
# Wed, 13 Mar 2024 01:15:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:15:09 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:15:09 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:15:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0bf838b872f1e012c580bbff8d1e66a09a7b05a85651db222851ea3323dab3d2`  
		Last Modified: Wed, 13 Mar 2024 01:16:47 GMT  
		Size: 5.4 MB (5430321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668de88817078f4ef2cf284dff428f40567f94b7132efee56fe3abe6264e6d42`  
		Last Modified: Wed, 13 Mar 2024 01:16:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore`

```console
$ docker pull nats@sha256:d7d19aca6454b871d5135f9cc685694349f0f72c02f00641f749e391f828e8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats@sha256:7fa1366a0cee4e50f2a2402c01dd3ea274be364140f556693350356d0e2db63c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2131507333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3743311440c84bac2fc9c9e5e74770053c07f4480d2901f7abe6813c87cf4dae`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 02:18:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Mar 2024 02:18:28 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:18:29 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 02:18:30 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.12/nats-server-v2.10.12-windows-amd64.zip
# Wed, 13 Mar 2024 02:18:30 GMT
ENV NATS_SERVER_SHASUM=bc944f832fdc3eaa0072c0a5e278efd672cec394159661070e7aea4f5d483cbc
# Wed, 13 Mar 2024 02:19:47 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Mar 2024 02:21:44 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 13 Mar 2024 02:21:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Mar 2024 02:21:45 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 02:21:46 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Mar 2024 02:21:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e169e85f3c664d99b16235c550eb744e7e1421ceb3b4a239fd727321ccddc77`  
		Last Modified: Wed, 13 Mar 2024 02:26:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7cb8b6faf23b1820a39bd95d7664a27dd6143342b384e0331e51b7e7ba82b72`  
		Last Modified: Wed, 13 Mar 2024 02:26:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3886c92295e481a562d7a5fe9418c1de632210a05c19f06705629bc95800902`  
		Last Modified: Wed, 13 Mar 2024 02:26:10 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b851f5dbeec69a3c0b7cef01f0be439c3febe18363296e9980de2f7ba04d04ec`  
		Last Modified: Wed, 13 Mar 2024 02:26:10 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ac0c5c4d4063f650788f99bee2df77584d4cce33709529fbf1c1287c77e6b1`  
		Last Modified: Wed, 13 Mar 2024 02:26:10 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce303014e2084243978d691011a901e05e79a3dd3aca02f6bf15b0111f313ba`  
		Last Modified: Wed, 13 Mar 2024 02:26:10 GMT  
		Size: 445.8 KB (445828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209561aab82234ce8e269b77a1c45eb4d10f5c3d9ec877e078db4d5b72ab672c`  
		Last Modified: Wed, 13 Mar 2024 02:26:09 GMT  
		Size: 5.9 MB (5948270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b859631a59ecabb2bf06bbe8d86a2994232ad2d5852842b40363bf2bbb528cc7`  
		Last Modified: Wed, 13 Mar 2024 02:26:08 GMT  
		Size: 2.0 KB (1985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b5005070ee0dabaf577a0f2e898332aab7a1ec26da577b3d2ceb9ffeaaf343`  
		Last Modified: Wed, 13 Mar 2024 02:26:08 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4db2f7ed46b07e7feccb03f8e63ad91142de5165acf6c898a5aac89b0cd559`  
		Last Modified: Wed, 13 Mar 2024 02:26:08 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81813a03072d63cfbad1f640180a29dfc80c337f2a4ffeaeb116769574cda27`  
		Last Modified: Wed, 13 Mar 2024 02:26:08 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-1809`

```console
$ docker pull nats@sha256:d7d19aca6454b871d5135f9cc685694349f0f72c02f00641f749e391f828e8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats:2.10-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats@sha256:7fa1366a0cee4e50f2a2402c01dd3ea274be364140f556693350356d0e2db63c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2131507333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3743311440c84bac2fc9c9e5e74770053c07f4480d2901f7abe6813c87cf4dae`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 02:18:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Mar 2024 02:18:28 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:18:29 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 02:18:30 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.12/nats-server-v2.10.12-windows-amd64.zip
# Wed, 13 Mar 2024 02:18:30 GMT
ENV NATS_SERVER_SHASUM=bc944f832fdc3eaa0072c0a5e278efd672cec394159661070e7aea4f5d483cbc
# Wed, 13 Mar 2024 02:19:47 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Mar 2024 02:21:44 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 13 Mar 2024 02:21:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Mar 2024 02:21:45 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 02:21:46 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Mar 2024 02:21:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e169e85f3c664d99b16235c550eb744e7e1421ceb3b4a239fd727321ccddc77`  
		Last Modified: Wed, 13 Mar 2024 02:26:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7cb8b6faf23b1820a39bd95d7664a27dd6143342b384e0331e51b7e7ba82b72`  
		Last Modified: Wed, 13 Mar 2024 02:26:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3886c92295e481a562d7a5fe9418c1de632210a05c19f06705629bc95800902`  
		Last Modified: Wed, 13 Mar 2024 02:26:10 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b851f5dbeec69a3c0b7cef01f0be439c3febe18363296e9980de2f7ba04d04ec`  
		Last Modified: Wed, 13 Mar 2024 02:26:10 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ac0c5c4d4063f650788f99bee2df77584d4cce33709529fbf1c1287c77e6b1`  
		Last Modified: Wed, 13 Mar 2024 02:26:10 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce303014e2084243978d691011a901e05e79a3dd3aca02f6bf15b0111f313ba`  
		Last Modified: Wed, 13 Mar 2024 02:26:10 GMT  
		Size: 445.8 KB (445828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209561aab82234ce8e269b77a1c45eb4d10f5c3d9ec877e078db4d5b72ab672c`  
		Last Modified: Wed, 13 Mar 2024 02:26:09 GMT  
		Size: 5.9 MB (5948270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b859631a59ecabb2bf06bbe8d86a2994232ad2d5852842b40363bf2bbb528cc7`  
		Last Modified: Wed, 13 Mar 2024 02:26:08 GMT  
		Size: 2.0 KB (1985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b5005070ee0dabaf577a0f2e898332aab7a1ec26da577b3d2ceb9ffeaaf343`  
		Last Modified: Wed, 13 Mar 2024 02:26:08 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4db2f7ed46b07e7feccb03f8e63ad91142de5165acf6c898a5aac89b0cd559`  
		Last Modified: Wed, 13 Mar 2024 02:26:08 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81813a03072d63cfbad1f640180a29dfc80c337f2a4ffeaeb116769574cda27`  
		Last Modified: Wed, 13 Mar 2024 02:26:08 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.12`

```console
$ docker pull nats@sha256:9b1ee0caf5737f6b44b15da670b866900af4077d6ae6e2a170466e2e0fc68cb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5576; amd64

### `nats:2.10.12` - linux; amd64

```console
$ docker pull nats@sha256:6fb1a85021a8411e0470cca8a43d461db915d2df605657389c4f0595d2e42e91
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5548142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8780d448219e4996eb219326ba6943b7e05f04ab1189a6f1dcf2e013058e3e36`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:47:57 GMT
COPY file:33d3e4ce6e17dc907ca0b478996354d26d433431b7bf48ae5bef3ec2ea1359f1 in /nats-server 
# Wed, 13 Mar 2024 01:47:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:47:57 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:47:57 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:47:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce8539fabe7af34129953a073c64515d008d19eac52a820ef52368f6411e540d`  
		Last Modified: Wed, 13 Mar 2024 01:48:46 GMT  
		Size: 5.5 MB (5547633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5208dae10516783bd9b5be071d7f3d39c84e1138b3887856c85f570ec4f588c`  
		Last Modified: Wed, 13 Mar 2024 01:48:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.12` - linux; arm variant v6

```console
$ docker pull nats@sha256:b717fb731a88e81bdabf9b7eb28e2ee0fa423ff801dcd5819fb4ffaf217cb208
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5263761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51552a7d22c2c5ca2447ff2b4198de16cfdff9a116a3c54ef5af0d997a9469f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:49:35 GMT
COPY file:c24c6855bab6e8b64a222738f44249dd58afe5ec56a34cfd64493e736f5325df in /nats-server 
# Wed, 13 Mar 2024 00:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:49:35 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:49:35 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:49:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bc2b5fa4421ea8f446fd52c0a8e7c8c6e048dc4aa6a096fb60765aa281147267`  
		Last Modified: Wed, 13 Mar 2024 00:50:20 GMT  
		Size: 5.3 MB (5263253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652cf78472b592b1ea355485d1a353340ba41c0d01b26f15ffacc090db84d7bb`  
		Last Modified: Wed, 13 Mar 2024 00:50:19 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.12` - linux; arm variant v7

```console
$ docker pull nats@sha256:07d02d1f567ff67a36ece1f90364e466f099db860d2e8ec1f2143bec1c3710f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5956a4e3835d4532ea5cbfc23f7b2e2d96d15a877f42392feea63afa16be107b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:35:52 GMT
COPY file:6899efa16d7091375dc53de2fc1e5686e82569d9799d6cede2e40b0a8b6abb48 in /nats-server 
# Wed, 13 Mar 2024 00:35:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:35:52 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:35:52 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:35:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:68296288971fdb3ddfe9bfba9b6a79725a69e891fb82cd5708f088afaac9929f`  
		Last Modified: Wed, 13 Mar 2024 00:36:43 GMT  
		Size: 5.3 MB (5254529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652026202bce83174144280de06b0537518e9d13e1674ac88f0d7e8491a2e440`  
		Last Modified: Wed, 13 Mar 2024 00:36:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.12` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f8017338e2c0dd9d3adb17672dd8226d475d5c810fa5f742c27a1d77f6e0c0e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8216507954fc8ffbaa79f3aa0908756fb3b5e699a13215671cf23837d30ca343`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:40:40 GMT
COPY file:674069719b01a345db55aa1ea35485a8b6f0cf0eed465ae05a0c00073e2ab2ab in /nats-server 
# Wed, 13 Mar 2024 00:40:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:40:40 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:40:40 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:40:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d5466aeaf1139b432e415e6412234c167a91220e74d17f50be1a2de5b0fb1b21`  
		Last Modified: Wed, 13 Mar 2024 00:41:26 GMT  
		Size: 5.1 MB (5117178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562c0bd40d1b70ec911e4b7219f7867675e2ad1c67899a3643f13d261d792187`  
		Last Modified: Wed, 13 Mar 2024 00:41:25 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.12` - linux; ppc64le

```console
$ docker pull nats@sha256:e964ace9a5047268966aa2f1f2e10472325f21ac790016722c0a9090997a39f1
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a273f9d6d6aa560ff8df97aee7e4c13f87044f2be0081b07ba0f4a0fafd81a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 16 Feb 2024 19:24:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:29:00 GMT
COPY file:0e1c98477f605478a27423b67d1c7bf88d4b2a56d0696ea31430a8a59b294dd8 in /nats-server 
# Wed, 13 Mar 2024 01:29:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:29:01 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:29:01 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:29:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7eaf17599ba122502fe00d1cb4014722df0b46a83f614f9430f71b816a6999f8`  
		Last Modified: Wed, 13 Mar 2024 01:29:44 GMT  
		Size: 5.1 MB (5096748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b8d7d148d9f2f60c0b13204daf3a2f76ff85991d79fe4fd82aa842a3d77a1d`  
		Last Modified: Wed, 13 Mar 2024 01:29:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.12` - linux; s390x

```console
$ docker pull nats@sha256:21d23f9777f88070c60ce8bf669dd9169ad10d91ddae1f43c02b5419cc5fcbc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5430830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a9daecac5ba461be180b94ca61fe053ebe1e5c23af8e61522f1854982e6157`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:15:09 GMT
COPY file:cc94c349de0e266f428d63773845fb669334304c5fbcffeec57553d333126f22 in /nats-server 
# Wed, 13 Mar 2024 01:15:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:15:09 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:15:09 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:15:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0bf838b872f1e012c580bbff8d1e66a09a7b05a85651db222851ea3323dab3d2`  
		Last Modified: Wed, 13 Mar 2024 01:16:47 GMT  
		Size: 5.4 MB (5430321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668de88817078f4ef2cf284dff428f40567f94b7132efee56fe3abe6264e6d42`  
		Last Modified: Wed, 13 Mar 2024 01:16:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.12` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats@sha256:1bb4572909b97a5aea3e76230e9d09a1078a21d41ba7000bd5afbe5225fc1568
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110290182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a1f3d16c6f5aea885d55ec76e40c984ca8763448ae4b9b424ec4d5bec24fc8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 02:21:55 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:21:57 GMT
RUN cmd /S /C #(nop) COPY file:b8b09037eca4c9daccbaf940396fb084777535cdce4ec562f44c0b727cf16e3e in C:\nats-server.exe 
# Wed, 13 Mar 2024 02:21:57 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Mar 2024 02:21:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 02:21:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Mar 2024 02:21:59 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e772fbc90f54f9eab2951a9615b88e9eca8fc78909aba2cb3678cc214eb88ae2`  
		Last Modified: Wed, 13 Mar 2024 02:26:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9cd82df1e1baf71960c98c3ca3996de090e25ce522c16d07628ea7705a1c7b`  
		Last Modified: Wed, 13 Mar 2024 02:26:26 GMT  
		Size: 5.7 MB (5663658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce47417df81557c57ff79790516751ae140155b5d06e2f8538fcf4d7e94a1004`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c07d5748899da1f68ed98e7331fa02c4175552921ad31f2ec6ba40f208c69d`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89220da9dce87f2d7ea149e170563fa7bac7ae732a1b8c89f51d60e5da18020e`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78635ce16de8337563a88c3a78835fed97c207dc9254d2dc0d06594b9926b0e0`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.12-alpine`

```console
$ docker pull nats@sha256:7a3dedb2152d01809b0343a8fce27241d6eae68f65200a8e6da78d88ac4257a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10.12-alpine` - linux; amd64

```console
$ docker pull nats@sha256:04333a656bd283d8642c365f790bbd26a0dd2919a0d29dd75998776c6ef7207d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9577940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606a0820025fa72d87e550430e7c14c89557b69fecac16e732dbf2d3c0bcaa76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 01:47:48 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 01:47:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 01:47:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 01:47:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 01:47:51 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:47:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 01:47:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a35673fda7fb893fc2c187357a17a1c13cb7b1958fa8d97eee3155901c44fba`  
		Last Modified: Wed, 13 Mar 2024 01:48:27 GMT  
		Size: 6.2 MB (6168214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdf5efdff66ae170a3b780d793b6b5d821138b53926474870aebccb2af5ee57`  
		Last Modified: Wed, 13 Mar 2024 01:48:25 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c95813002da682382a4ba34c5210071c10314593a044ab5120d5d8780b07e4a`  
		Last Modified: Wed, 13 Mar 2024 01:48:25 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.12-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:6e93abf037354dbe3af08ece7d516f8a4e61c675fbab84594adf10b108082777
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9051274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075217343e913477fcd44713b6ae36fa6c55e5a333eca26c9e952a97e51a14f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 00:49:24 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 00:49:28 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 00:49:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 00:49:28 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 00:49:28 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:49:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 00:49:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b7bd072e2424f96ed51dee5137cd95e43686fc4624f2d2feee365fd304f5fc`  
		Last Modified: Wed, 13 Mar 2024 00:50:00 GMT  
		Size: 5.9 MB (5884880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cd491dd798da6f6a27555feb3be80ea1e29262571e10acde00300ee332740f`  
		Last Modified: Wed, 13 Mar 2024 00:49:59 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568e37ef91f5962c31828a2adc1588dcec32dbe5859699372ff1656c5659a915`  
		Last Modified: Wed, 13 Mar 2024 00:49:59 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.12-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:06913e056cdc6c1997068e0fe2e6355f571c04f12afd48f9e02cea1f16554016
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8795654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fbc0f10b6a6c92c2a77318fa3a4f9b73f5dc9a8e0304b5475f614294196d6d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 00:35:35 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 00:35:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 00:35:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 00:35:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 00:35:39 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:35:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 00:35:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55a741d01acaf5448cb8ffa39243f9f34261fd88e914772554124224189cc81`  
		Last Modified: Wed, 13 Mar 2024 00:36:23 GMT  
		Size: 5.9 MB (5875752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d61266118e4acdda142cd2ac76a4ef35e24e7502ec60b4cf26cf49a145acdc`  
		Last Modified: Wed, 13 Mar 2024 00:36:18 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1e59e375c0cd803e4186b41a2566a69e1f0a8b88ba1cf0954a5a00d33af0d2`  
		Last Modified: Wed, 13 Mar 2024 00:36:18 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.12-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:62b700c1d94d9c9164795d902681026f20a4c2c215e70dea7661f632c43f93b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9088728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b8a7d9375b33a34c6019c8a05fc253872624aaba1066208fa1ae728471c370`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 00:40:21 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 00:40:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 00:40:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 00:40:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 00:40:24 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:40:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 00:40:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46909e9837d35c1cb85abbf0a81ed8df7ac00f9ac7df67d275bd7edb87fdc88b`  
		Last Modified: Wed, 13 Mar 2024 00:41:06 GMT  
		Size: 5.7 MB (5740016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a74044cf86ca3325a7a324fbd7d08694e721bad44f2f7865d35ed3b3ce23b4`  
		Last Modified: Wed, 13 Mar 2024 00:41:05 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f776b77a6001c5e0fd42db5610aa2acfeecb867c59a3559a2cd6983a5067ad6c`  
		Last Modified: Wed, 13 Mar 2024 00:41:05 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.12-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:e73b5c826fe9e8fc554f8e4440d8ae0504b4f7899d6c5bc38c6b68a0d9e705d0
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9078995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96541c86763ab33908efa9617f909b1b23853fc66f5740829aaa97d4fb819d4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 01:28:25 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 01:28:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 01:28:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 01:28:31 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 01:28:32 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:28:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 01:28:33 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd4d0c36112be2592baa66fdba8327cff756029be8e96f803015fce9a8bfab7`  
		Last Modified: Wed, 13 Mar 2024 01:29:22 GMT  
		Size: 5.7 MB (5719643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217c8e169d797596a8b822f912ec2ba564e491f6949ecd95a5a405d275c5a5a6`  
		Last Modified: Wed, 13 Mar 2024 01:29:21 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad20a946927156b80304d831d9d123a0ba902501570002869968e92231bbd32`  
		Last Modified: Wed, 13 Mar 2024 01:29:21 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.12-alpine` - linux; s390x

```console
$ docker pull nats@sha256:49f1c4fa564a8f8073315103db29d373273c7e703c43d6f275a1acc3ab010a3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9296162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7420d0049b07e2c363f050c33e0ac3ba0fe39fe6d0bee0ffea5c71f2fdf0749`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 01:14:00 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 01:14:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 01:14:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 01:14:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 01:14:03 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:14:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 01:14:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d4a8da7be6313cc596f154b85b638749ab970144f58575af5bef288a9e44ce`  
		Last Modified: Wed, 13 Mar 2024 01:16:34 GMT  
		Size: 6.1 MB (6052529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c87220ce1b5f8a7ed2e5ab6caf39ac9028ba6d25133711633f25a21b60c4b24`  
		Last Modified: Wed, 13 Mar 2024 01:16:33 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43f30dc994a90cc1c2a38e8a5176d279817dd3d25ffe3d8ac67b665c606f3b3`  
		Last Modified: Wed, 13 Mar 2024 01:16:33 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.12-alpine3.19`

```console
$ docker pull nats@sha256:7a3dedb2152d01809b0343a8fce27241d6eae68f65200a8e6da78d88ac4257a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10.12-alpine3.19` - linux; amd64

```console
$ docker pull nats@sha256:04333a656bd283d8642c365f790bbd26a0dd2919a0d29dd75998776c6ef7207d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9577940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606a0820025fa72d87e550430e7c14c89557b69fecac16e732dbf2d3c0bcaa76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 01:47:48 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 01:47:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 01:47:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 01:47:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 01:47:51 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:47:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 01:47:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a35673fda7fb893fc2c187357a17a1c13cb7b1958fa8d97eee3155901c44fba`  
		Last Modified: Wed, 13 Mar 2024 01:48:27 GMT  
		Size: 6.2 MB (6168214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdf5efdff66ae170a3b780d793b6b5d821138b53926474870aebccb2af5ee57`  
		Last Modified: Wed, 13 Mar 2024 01:48:25 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c95813002da682382a4ba34c5210071c10314593a044ab5120d5d8780b07e4a`  
		Last Modified: Wed, 13 Mar 2024 01:48:25 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.12-alpine3.19` - linux; arm variant v6

```console
$ docker pull nats@sha256:6e93abf037354dbe3af08ece7d516f8a4e61c675fbab84594adf10b108082777
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9051274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075217343e913477fcd44713b6ae36fa6c55e5a333eca26c9e952a97e51a14f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 00:49:24 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 00:49:28 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 00:49:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 00:49:28 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 00:49:28 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:49:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 00:49:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b7bd072e2424f96ed51dee5137cd95e43686fc4624f2d2feee365fd304f5fc`  
		Last Modified: Wed, 13 Mar 2024 00:50:00 GMT  
		Size: 5.9 MB (5884880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cd491dd798da6f6a27555feb3be80ea1e29262571e10acde00300ee332740f`  
		Last Modified: Wed, 13 Mar 2024 00:49:59 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568e37ef91f5962c31828a2adc1588dcec32dbe5859699372ff1656c5659a915`  
		Last Modified: Wed, 13 Mar 2024 00:49:59 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.12-alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:06913e056cdc6c1997068e0fe2e6355f571c04f12afd48f9e02cea1f16554016
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8795654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fbc0f10b6a6c92c2a77318fa3a4f9b73f5dc9a8e0304b5475f614294196d6d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 00:35:35 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 00:35:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 00:35:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 00:35:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 00:35:39 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:35:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 00:35:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55a741d01acaf5448cb8ffa39243f9f34261fd88e914772554124224189cc81`  
		Last Modified: Wed, 13 Mar 2024 00:36:23 GMT  
		Size: 5.9 MB (5875752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d61266118e4acdda142cd2ac76a4ef35e24e7502ec60b4cf26cf49a145acdc`  
		Last Modified: Wed, 13 Mar 2024 00:36:18 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1e59e375c0cd803e4186b41a2566a69e1f0a8b88ba1cf0954a5a00d33af0d2`  
		Last Modified: Wed, 13 Mar 2024 00:36:18 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.12-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:62b700c1d94d9c9164795d902681026f20a4c2c215e70dea7661f632c43f93b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9088728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b8a7d9375b33a34c6019c8a05fc253872624aaba1066208fa1ae728471c370`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 00:40:21 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 00:40:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 00:40:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 00:40:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 00:40:24 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:40:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 00:40:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46909e9837d35c1cb85abbf0a81ed8df7ac00f9ac7df67d275bd7edb87fdc88b`  
		Last Modified: Wed, 13 Mar 2024 00:41:06 GMT  
		Size: 5.7 MB (5740016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a74044cf86ca3325a7a324fbd7d08694e721bad44f2f7865d35ed3b3ce23b4`  
		Last Modified: Wed, 13 Mar 2024 00:41:05 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f776b77a6001c5e0fd42db5610aa2acfeecb867c59a3559a2cd6983a5067ad6c`  
		Last Modified: Wed, 13 Mar 2024 00:41:05 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.12-alpine3.19` - linux; ppc64le

```console
$ docker pull nats@sha256:e73b5c826fe9e8fc554f8e4440d8ae0504b4f7899d6c5bc38c6b68a0d9e705d0
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9078995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96541c86763ab33908efa9617f909b1b23853fc66f5740829aaa97d4fb819d4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 01:28:25 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 01:28:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 01:28:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 01:28:31 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 01:28:32 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:28:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 01:28:33 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd4d0c36112be2592baa66fdba8327cff756029be8e96f803015fce9a8bfab7`  
		Last Modified: Wed, 13 Mar 2024 01:29:22 GMT  
		Size: 5.7 MB (5719643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217c8e169d797596a8b822f912ec2ba564e491f6949ecd95a5a405d275c5a5a6`  
		Last Modified: Wed, 13 Mar 2024 01:29:21 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad20a946927156b80304d831d9d123a0ba902501570002869968e92231bbd32`  
		Last Modified: Wed, 13 Mar 2024 01:29:21 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.12-alpine3.19` - linux; s390x

```console
$ docker pull nats@sha256:49f1c4fa564a8f8073315103db29d373273c7e703c43d6f275a1acc3ab010a3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9296162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7420d0049b07e2c363f050c33e0ac3ba0fe39fe6d0bee0ffea5c71f2fdf0749`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 01:14:00 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 01:14:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 01:14:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 01:14:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 01:14:03 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:14:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 01:14:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d4a8da7be6313cc596f154b85b638749ab970144f58575af5bef288a9e44ce`  
		Last Modified: Wed, 13 Mar 2024 01:16:34 GMT  
		Size: 6.1 MB (6052529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c87220ce1b5f8a7ed2e5ab6caf39ac9028ba6d25133711633f25a21b60c4b24`  
		Last Modified: Wed, 13 Mar 2024 01:16:33 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43f30dc994a90cc1c2a38e8a5176d279817dd3d25ffe3d8ac67b665c606f3b3`  
		Last Modified: Wed, 13 Mar 2024 01:16:33 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.12-linux`

```console
$ docker pull nats@sha256:bb90d21b87ba223e838d39e5ee66ebeea8b63e8a6bffb4a2b19f5b291e46d1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10.12-linux` - linux; amd64

```console
$ docker pull nats@sha256:6fb1a85021a8411e0470cca8a43d461db915d2df605657389c4f0595d2e42e91
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5548142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8780d448219e4996eb219326ba6943b7e05f04ab1189a6f1dcf2e013058e3e36`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:47:57 GMT
COPY file:33d3e4ce6e17dc907ca0b478996354d26d433431b7bf48ae5bef3ec2ea1359f1 in /nats-server 
# Wed, 13 Mar 2024 01:47:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:47:57 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:47:57 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:47:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce8539fabe7af34129953a073c64515d008d19eac52a820ef52368f6411e540d`  
		Last Modified: Wed, 13 Mar 2024 01:48:46 GMT  
		Size: 5.5 MB (5547633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5208dae10516783bd9b5be071d7f3d39c84e1138b3887856c85f570ec4f588c`  
		Last Modified: Wed, 13 Mar 2024 01:48:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.12-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:b717fb731a88e81bdabf9b7eb28e2ee0fa423ff801dcd5819fb4ffaf217cb208
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5263761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51552a7d22c2c5ca2447ff2b4198de16cfdff9a116a3c54ef5af0d997a9469f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:49:35 GMT
COPY file:c24c6855bab6e8b64a222738f44249dd58afe5ec56a34cfd64493e736f5325df in /nats-server 
# Wed, 13 Mar 2024 00:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:49:35 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:49:35 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:49:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bc2b5fa4421ea8f446fd52c0a8e7c8c6e048dc4aa6a096fb60765aa281147267`  
		Last Modified: Wed, 13 Mar 2024 00:50:20 GMT  
		Size: 5.3 MB (5263253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652cf78472b592b1ea355485d1a353340ba41c0d01b26f15ffacc090db84d7bb`  
		Last Modified: Wed, 13 Mar 2024 00:50:19 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.12-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:07d02d1f567ff67a36ece1f90364e466f099db860d2e8ec1f2143bec1c3710f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5956a4e3835d4532ea5cbfc23f7b2e2d96d15a877f42392feea63afa16be107b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:35:52 GMT
COPY file:6899efa16d7091375dc53de2fc1e5686e82569d9799d6cede2e40b0a8b6abb48 in /nats-server 
# Wed, 13 Mar 2024 00:35:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:35:52 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:35:52 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:35:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:68296288971fdb3ddfe9bfba9b6a79725a69e891fb82cd5708f088afaac9929f`  
		Last Modified: Wed, 13 Mar 2024 00:36:43 GMT  
		Size: 5.3 MB (5254529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652026202bce83174144280de06b0537518e9d13e1674ac88f0d7e8491a2e440`  
		Last Modified: Wed, 13 Mar 2024 00:36:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.12-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f8017338e2c0dd9d3adb17672dd8226d475d5c810fa5f742c27a1d77f6e0c0e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8216507954fc8ffbaa79f3aa0908756fb3b5e699a13215671cf23837d30ca343`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:40:40 GMT
COPY file:674069719b01a345db55aa1ea35485a8b6f0cf0eed465ae05a0c00073e2ab2ab in /nats-server 
# Wed, 13 Mar 2024 00:40:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:40:40 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:40:40 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:40:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d5466aeaf1139b432e415e6412234c167a91220e74d17f50be1a2de5b0fb1b21`  
		Last Modified: Wed, 13 Mar 2024 00:41:26 GMT  
		Size: 5.1 MB (5117178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562c0bd40d1b70ec911e4b7219f7867675e2ad1c67899a3643f13d261d792187`  
		Last Modified: Wed, 13 Mar 2024 00:41:25 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.12-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:e964ace9a5047268966aa2f1f2e10472325f21ac790016722c0a9090997a39f1
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a273f9d6d6aa560ff8df97aee7e4c13f87044f2be0081b07ba0f4a0fafd81a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 16 Feb 2024 19:24:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:29:00 GMT
COPY file:0e1c98477f605478a27423b67d1c7bf88d4b2a56d0696ea31430a8a59b294dd8 in /nats-server 
# Wed, 13 Mar 2024 01:29:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:29:01 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:29:01 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:29:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7eaf17599ba122502fe00d1cb4014722df0b46a83f614f9430f71b816a6999f8`  
		Last Modified: Wed, 13 Mar 2024 01:29:44 GMT  
		Size: 5.1 MB (5096748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b8d7d148d9f2f60c0b13204daf3a2f76ff85991d79fe4fd82aa842a3d77a1d`  
		Last Modified: Wed, 13 Mar 2024 01:29:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.12-linux` - linux; s390x

```console
$ docker pull nats@sha256:21d23f9777f88070c60ce8bf669dd9169ad10d91ddae1f43c02b5419cc5fcbc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5430830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a9daecac5ba461be180b94ca61fe053ebe1e5c23af8e61522f1854982e6157`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:15:09 GMT
COPY file:cc94c349de0e266f428d63773845fb669334304c5fbcffeec57553d333126f22 in /nats-server 
# Wed, 13 Mar 2024 01:15:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:15:09 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:15:09 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:15:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0bf838b872f1e012c580bbff8d1e66a09a7b05a85651db222851ea3323dab3d2`  
		Last Modified: Wed, 13 Mar 2024 01:16:47 GMT  
		Size: 5.4 MB (5430321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668de88817078f4ef2cf284dff428f40567f94b7132efee56fe3abe6264e6d42`  
		Last Modified: Wed, 13 Mar 2024 01:16:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.12-nanoserver`

```console
$ docker pull nats@sha256:38b381e6f2834d3c5120087f02c9d13f238a2142f54568a208fa74d554bb62d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats:2.10.12-nanoserver` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats@sha256:1bb4572909b97a5aea3e76230e9d09a1078a21d41ba7000bd5afbe5225fc1568
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110290182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a1f3d16c6f5aea885d55ec76e40c984ca8763448ae4b9b424ec4d5bec24fc8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 02:21:55 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:21:57 GMT
RUN cmd /S /C #(nop) COPY file:b8b09037eca4c9daccbaf940396fb084777535cdce4ec562f44c0b727cf16e3e in C:\nats-server.exe 
# Wed, 13 Mar 2024 02:21:57 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Mar 2024 02:21:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 02:21:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Mar 2024 02:21:59 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e772fbc90f54f9eab2951a9615b88e9eca8fc78909aba2cb3678cc214eb88ae2`  
		Last Modified: Wed, 13 Mar 2024 02:26:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9cd82df1e1baf71960c98c3ca3996de090e25ce522c16d07628ea7705a1c7b`  
		Last Modified: Wed, 13 Mar 2024 02:26:26 GMT  
		Size: 5.7 MB (5663658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce47417df81557c57ff79790516751ae140155b5d06e2f8538fcf4d7e94a1004`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c07d5748899da1f68ed98e7331fa02c4175552921ad31f2ec6ba40f208c69d`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89220da9dce87f2d7ea149e170563fa7bac7ae732a1b8c89f51d60e5da18020e`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78635ce16de8337563a88c3a78835fed97c207dc9254d2dc0d06594b9926b0e0`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.12-nanoserver-1809`

```console
$ docker pull nats@sha256:38b381e6f2834d3c5120087f02c9d13f238a2142f54568a208fa74d554bb62d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats:2.10.12-nanoserver-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats@sha256:1bb4572909b97a5aea3e76230e9d09a1078a21d41ba7000bd5afbe5225fc1568
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110290182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a1f3d16c6f5aea885d55ec76e40c984ca8763448ae4b9b424ec4d5bec24fc8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 02:21:55 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:21:57 GMT
RUN cmd /S /C #(nop) COPY file:b8b09037eca4c9daccbaf940396fb084777535cdce4ec562f44c0b727cf16e3e in C:\nats-server.exe 
# Wed, 13 Mar 2024 02:21:57 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Mar 2024 02:21:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 02:21:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Mar 2024 02:21:59 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e772fbc90f54f9eab2951a9615b88e9eca8fc78909aba2cb3678cc214eb88ae2`  
		Last Modified: Wed, 13 Mar 2024 02:26:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9cd82df1e1baf71960c98c3ca3996de090e25ce522c16d07628ea7705a1c7b`  
		Last Modified: Wed, 13 Mar 2024 02:26:26 GMT  
		Size: 5.7 MB (5663658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce47417df81557c57ff79790516751ae140155b5d06e2f8538fcf4d7e94a1004`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c07d5748899da1f68ed98e7331fa02c4175552921ad31f2ec6ba40f208c69d`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89220da9dce87f2d7ea149e170563fa7bac7ae732a1b8c89f51d60e5da18020e`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78635ce16de8337563a88c3a78835fed97c207dc9254d2dc0d06594b9926b0e0`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.12-scratch`

```console
$ docker pull nats@sha256:bb90d21b87ba223e838d39e5ee66ebeea8b63e8a6bffb4a2b19f5b291e46d1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10.12-scratch` - linux; amd64

```console
$ docker pull nats@sha256:6fb1a85021a8411e0470cca8a43d461db915d2df605657389c4f0595d2e42e91
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5548142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8780d448219e4996eb219326ba6943b7e05f04ab1189a6f1dcf2e013058e3e36`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:47:57 GMT
COPY file:33d3e4ce6e17dc907ca0b478996354d26d433431b7bf48ae5bef3ec2ea1359f1 in /nats-server 
# Wed, 13 Mar 2024 01:47:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:47:57 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:47:57 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:47:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce8539fabe7af34129953a073c64515d008d19eac52a820ef52368f6411e540d`  
		Last Modified: Wed, 13 Mar 2024 01:48:46 GMT  
		Size: 5.5 MB (5547633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5208dae10516783bd9b5be071d7f3d39c84e1138b3887856c85f570ec4f588c`  
		Last Modified: Wed, 13 Mar 2024 01:48:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.12-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:b717fb731a88e81bdabf9b7eb28e2ee0fa423ff801dcd5819fb4ffaf217cb208
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5263761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51552a7d22c2c5ca2447ff2b4198de16cfdff9a116a3c54ef5af0d997a9469f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:49:35 GMT
COPY file:c24c6855bab6e8b64a222738f44249dd58afe5ec56a34cfd64493e736f5325df in /nats-server 
# Wed, 13 Mar 2024 00:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:49:35 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:49:35 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:49:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bc2b5fa4421ea8f446fd52c0a8e7c8c6e048dc4aa6a096fb60765aa281147267`  
		Last Modified: Wed, 13 Mar 2024 00:50:20 GMT  
		Size: 5.3 MB (5263253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652cf78472b592b1ea355485d1a353340ba41c0d01b26f15ffacc090db84d7bb`  
		Last Modified: Wed, 13 Mar 2024 00:50:19 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.12-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:07d02d1f567ff67a36ece1f90364e466f099db860d2e8ec1f2143bec1c3710f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5956a4e3835d4532ea5cbfc23f7b2e2d96d15a877f42392feea63afa16be107b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:35:52 GMT
COPY file:6899efa16d7091375dc53de2fc1e5686e82569d9799d6cede2e40b0a8b6abb48 in /nats-server 
# Wed, 13 Mar 2024 00:35:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:35:52 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:35:52 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:35:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:68296288971fdb3ddfe9bfba9b6a79725a69e891fb82cd5708f088afaac9929f`  
		Last Modified: Wed, 13 Mar 2024 00:36:43 GMT  
		Size: 5.3 MB (5254529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652026202bce83174144280de06b0537518e9d13e1674ac88f0d7e8491a2e440`  
		Last Modified: Wed, 13 Mar 2024 00:36:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.12-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f8017338e2c0dd9d3adb17672dd8226d475d5c810fa5f742c27a1d77f6e0c0e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8216507954fc8ffbaa79f3aa0908756fb3b5e699a13215671cf23837d30ca343`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:40:40 GMT
COPY file:674069719b01a345db55aa1ea35485a8b6f0cf0eed465ae05a0c00073e2ab2ab in /nats-server 
# Wed, 13 Mar 2024 00:40:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:40:40 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:40:40 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:40:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d5466aeaf1139b432e415e6412234c167a91220e74d17f50be1a2de5b0fb1b21`  
		Last Modified: Wed, 13 Mar 2024 00:41:26 GMT  
		Size: 5.1 MB (5117178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562c0bd40d1b70ec911e4b7219f7867675e2ad1c67899a3643f13d261d792187`  
		Last Modified: Wed, 13 Mar 2024 00:41:25 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.12-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:e964ace9a5047268966aa2f1f2e10472325f21ac790016722c0a9090997a39f1
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a273f9d6d6aa560ff8df97aee7e4c13f87044f2be0081b07ba0f4a0fafd81a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 16 Feb 2024 19:24:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:29:00 GMT
COPY file:0e1c98477f605478a27423b67d1c7bf88d4b2a56d0696ea31430a8a59b294dd8 in /nats-server 
# Wed, 13 Mar 2024 01:29:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:29:01 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:29:01 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:29:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7eaf17599ba122502fe00d1cb4014722df0b46a83f614f9430f71b816a6999f8`  
		Last Modified: Wed, 13 Mar 2024 01:29:44 GMT  
		Size: 5.1 MB (5096748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b8d7d148d9f2f60c0b13204daf3a2f76ff85991d79fe4fd82aa842a3d77a1d`  
		Last Modified: Wed, 13 Mar 2024 01:29:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.12-scratch` - linux; s390x

```console
$ docker pull nats@sha256:21d23f9777f88070c60ce8bf669dd9169ad10d91ddae1f43c02b5419cc5fcbc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5430830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a9daecac5ba461be180b94ca61fe053ebe1e5c23af8e61522f1854982e6157`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:15:09 GMT
COPY file:cc94c349de0e266f428d63773845fb669334304c5fbcffeec57553d333126f22 in /nats-server 
# Wed, 13 Mar 2024 01:15:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:15:09 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:15:09 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:15:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0bf838b872f1e012c580bbff8d1e66a09a7b05a85651db222851ea3323dab3d2`  
		Last Modified: Wed, 13 Mar 2024 01:16:47 GMT  
		Size: 5.4 MB (5430321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668de88817078f4ef2cf284dff428f40567f94b7132efee56fe3abe6264e6d42`  
		Last Modified: Wed, 13 Mar 2024 01:16:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.12-windowsservercore`

```console
$ docker pull nats@sha256:d7d19aca6454b871d5135f9cc685694349f0f72c02f00641f749e391f828e8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats:2.10.12-windowsservercore` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats@sha256:7fa1366a0cee4e50f2a2402c01dd3ea274be364140f556693350356d0e2db63c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2131507333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3743311440c84bac2fc9c9e5e74770053c07f4480d2901f7abe6813c87cf4dae`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 02:18:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Mar 2024 02:18:28 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:18:29 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 02:18:30 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.12/nats-server-v2.10.12-windows-amd64.zip
# Wed, 13 Mar 2024 02:18:30 GMT
ENV NATS_SERVER_SHASUM=bc944f832fdc3eaa0072c0a5e278efd672cec394159661070e7aea4f5d483cbc
# Wed, 13 Mar 2024 02:19:47 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Mar 2024 02:21:44 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 13 Mar 2024 02:21:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Mar 2024 02:21:45 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 02:21:46 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Mar 2024 02:21:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e169e85f3c664d99b16235c550eb744e7e1421ceb3b4a239fd727321ccddc77`  
		Last Modified: Wed, 13 Mar 2024 02:26:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7cb8b6faf23b1820a39bd95d7664a27dd6143342b384e0331e51b7e7ba82b72`  
		Last Modified: Wed, 13 Mar 2024 02:26:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3886c92295e481a562d7a5fe9418c1de632210a05c19f06705629bc95800902`  
		Last Modified: Wed, 13 Mar 2024 02:26:10 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b851f5dbeec69a3c0b7cef01f0be439c3febe18363296e9980de2f7ba04d04ec`  
		Last Modified: Wed, 13 Mar 2024 02:26:10 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ac0c5c4d4063f650788f99bee2df77584d4cce33709529fbf1c1287c77e6b1`  
		Last Modified: Wed, 13 Mar 2024 02:26:10 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce303014e2084243978d691011a901e05e79a3dd3aca02f6bf15b0111f313ba`  
		Last Modified: Wed, 13 Mar 2024 02:26:10 GMT  
		Size: 445.8 KB (445828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209561aab82234ce8e269b77a1c45eb4d10f5c3d9ec877e078db4d5b72ab672c`  
		Last Modified: Wed, 13 Mar 2024 02:26:09 GMT  
		Size: 5.9 MB (5948270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b859631a59ecabb2bf06bbe8d86a2994232ad2d5852842b40363bf2bbb528cc7`  
		Last Modified: Wed, 13 Mar 2024 02:26:08 GMT  
		Size: 2.0 KB (1985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b5005070ee0dabaf577a0f2e898332aab7a1ec26da577b3d2ceb9ffeaaf343`  
		Last Modified: Wed, 13 Mar 2024 02:26:08 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4db2f7ed46b07e7feccb03f8e63ad91142de5165acf6c898a5aac89b0cd559`  
		Last Modified: Wed, 13 Mar 2024 02:26:08 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81813a03072d63cfbad1f640180a29dfc80c337f2a4ffeaeb116769574cda27`  
		Last Modified: Wed, 13 Mar 2024 02:26:08 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.12-windowsservercore-1809`

```console
$ docker pull nats@sha256:d7d19aca6454b871d5135f9cc685694349f0f72c02f00641f749e391f828e8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats:2.10.12-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats@sha256:7fa1366a0cee4e50f2a2402c01dd3ea274be364140f556693350356d0e2db63c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2131507333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3743311440c84bac2fc9c9e5e74770053c07f4480d2901f7abe6813c87cf4dae`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 02:18:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Mar 2024 02:18:28 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:18:29 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 02:18:30 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.12/nats-server-v2.10.12-windows-amd64.zip
# Wed, 13 Mar 2024 02:18:30 GMT
ENV NATS_SERVER_SHASUM=bc944f832fdc3eaa0072c0a5e278efd672cec394159661070e7aea4f5d483cbc
# Wed, 13 Mar 2024 02:19:47 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Mar 2024 02:21:44 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 13 Mar 2024 02:21:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Mar 2024 02:21:45 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 02:21:46 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Mar 2024 02:21:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e169e85f3c664d99b16235c550eb744e7e1421ceb3b4a239fd727321ccddc77`  
		Last Modified: Wed, 13 Mar 2024 02:26:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7cb8b6faf23b1820a39bd95d7664a27dd6143342b384e0331e51b7e7ba82b72`  
		Last Modified: Wed, 13 Mar 2024 02:26:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3886c92295e481a562d7a5fe9418c1de632210a05c19f06705629bc95800902`  
		Last Modified: Wed, 13 Mar 2024 02:26:10 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b851f5dbeec69a3c0b7cef01f0be439c3febe18363296e9980de2f7ba04d04ec`  
		Last Modified: Wed, 13 Mar 2024 02:26:10 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ac0c5c4d4063f650788f99bee2df77584d4cce33709529fbf1c1287c77e6b1`  
		Last Modified: Wed, 13 Mar 2024 02:26:10 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce303014e2084243978d691011a901e05e79a3dd3aca02f6bf15b0111f313ba`  
		Last Modified: Wed, 13 Mar 2024 02:26:10 GMT  
		Size: 445.8 KB (445828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209561aab82234ce8e269b77a1c45eb4d10f5c3d9ec877e078db4d5b72ab672c`  
		Last Modified: Wed, 13 Mar 2024 02:26:09 GMT  
		Size: 5.9 MB (5948270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b859631a59ecabb2bf06bbe8d86a2994232ad2d5852842b40363bf2bbb528cc7`  
		Last Modified: Wed, 13 Mar 2024 02:26:08 GMT  
		Size: 2.0 KB (1985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b5005070ee0dabaf577a0f2e898332aab7a1ec26da577b3d2ceb9ffeaaf343`  
		Last Modified: Wed, 13 Mar 2024 02:26:08 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4db2f7ed46b07e7feccb03f8e63ad91142de5165acf6c898a5aac89b0cd559`  
		Last Modified: Wed, 13 Mar 2024 02:26:08 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81813a03072d63cfbad1f640180a29dfc80c337f2a4ffeaeb116769574cda27`  
		Last Modified: Wed, 13 Mar 2024 02:26:08 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9`

```console
$ docker pull nats@sha256:0a82ff2655b58da57640830854cc737d3d11b576feff75cfebbeba6c816a9b6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9` - linux; amd64

```console
$ docker pull nats@sha256:a7e4a1ba3c39879534d979369e31ec8818a48ead1ba701c582b5d6e352633504
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f668a6e8b2011067cca2504c059f26a5a7c06041892e8ba5b714d710cb9bd826`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 Mar 2024 19:20:44 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Fri, 01 Mar 2024 19:20:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 01 Mar 2024 19:20:44 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:20:45 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 Mar 2024 19:20:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f699f223b48ced53c4ba45eeb6d1ac552aa28bf511fc0df9ae5c4c3a65c971ba`  
		Last Modified: Fri, 01 Mar 2024 19:21:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v6

```console
$ docker pull nats@sha256:4576f0b4cb82774a99d4042d21706c0520ce243e70e3f96a060582ec8f72f6a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77c382d3556ef41f298f7d208a816a5396fd07a0d6c5760dd20b10e929d33a1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 Mar 2024 19:35:14 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Fri, 01 Mar 2024 19:35:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 01 Mar 2024 19:35:14 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:35:14 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 Mar 2024 19:35:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ac152519d53c3088e03edd635f8549e9cab54891c40718081ce170cf339d4c`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v7

```console
$ docker pull nats@sha256:2d00f74b5e4925e094e8c255bd54b9ba990dfbb5a8075b8deefe157ab776f6a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ef38d849c572b0ea5b33edd7fc7159a4f23e6d7ec34f61f36e9f16318289c7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 Mar 2024 19:29:31 GMT
COPY file:f989a3b6b3046a59c074559b413150c95cf8d5d1ad18593e3196fb2358872062 in /nats-server 
# Fri, 01 Mar 2024 19:29:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 01 Mar 2024 19:29:31 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:29:32 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 Mar 2024 19:29:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27bc08b69112c5d2b1303c6851c8f28dabd07a534f6cbd40dd483f3b42592d2`  
		Last Modified: Fri, 01 Mar 2024 19:30:15 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:0552a257c7e45b31aed00e37608ef4385b9714e9df68c036b6e5616d008f5fbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4786381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3c06731f019f3225f45063fe5eb50a27f4f5eab3a5f0f12b643c25a17a342f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 Mar 2024 19:40:20 GMT
COPY file:9f4f9739ea11f1ae7dd58ca32aa05c035fc77596540ec47bb5bc6d740714b029 in /nats-server 
# Fri, 01 Mar 2024 19:40:20 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 01 Mar 2024 19:40:20 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:40:20 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 Mar 2024 19:40:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee63d7485e86263b322f1514b9465e29e85b0c63a9841f6221a71833eb8dd33f`  
		Last Modified: Fri, 01 Mar 2024 19:41:00 GMT  
		Size: 4.8 MB (4785873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76ab54766965e7e61847c4162711672786e627368e813179d7fd5efa6da087b`  
		Last Modified: Fri, 01 Mar 2024 19:40:59 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine`

```console
$ docker pull nats@sha256:aeabd56ea61bac76bfed034f6cd174ec5c67b9224d2492368cfc24909594412c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine` - linux; amd64

```console
$ docker pull nats@sha256:98626a6255a2e27f6d2ddec17334d5a0046d63e0248c7a15518ebafb08598792
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9bdf51c21f823de1be2eff2f66d47cab646e69abd993ac29ce36ff1b615e95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Fri, 01 Mar 2024 19:20:36 GMT
ENV NATS_SERVER=2.9.25
# Fri, 01 Mar 2024 19:20:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 01 Mar 2024 19:20:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 01 Mar 2024 19:20:38 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 01 Mar 2024 19:20:38 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:20:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Mar 2024 19:20:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7725f62690c33c886fe27001486c543e1c50b5daf8c01573c3ab81a14c6f8d6a`  
		Last Modified: Fri, 01 Mar 2024 19:21:17 GMT  
		Size: 5.9 MB (5870706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63da9b0552d29d7213701b52a2e694569aa55262c6b47bad12863843434224b0`  
		Last Modified: Fri, 01 Mar 2024 19:21:16 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b5c9d61be8d0316e11d04da18e299abd7c27033460f7db0c3c5750e37387f6`  
		Last Modified: Fri, 01 Mar 2024 19:21:16 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:ea4229e8bb324a257fcddf953610d47ca443186fa8366ac6a5f61a9f1b4bdddd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8755242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b924a50cd5fb602a79fb5ed81445937bb67c1e9d01eb05b9ebc4ae2a5ca414a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Fri, 01 Mar 2024 19:35:07 GMT
ENV NATS_SERVER=2.9.25
# Fri, 01 Mar 2024 19:35:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 01 Mar 2024 19:35:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 01 Mar 2024 19:35:10 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 01 Mar 2024 19:35:11 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:35:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Mar 2024 19:35:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d68ec422dee341bb1f4eb7e01dec24854079424aa33eddc2d0cea72669144a`  
		Last Modified: Fri, 01 Mar 2024 19:35:40 GMT  
		Size: 5.6 MB (5607183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43baee7c50e69ffb5fb9c14225c9643a0b92cdf44a40a62a716de40b692708b1`  
		Last Modified: Fri, 01 Mar 2024 19:35:39 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e86a76ef5558f8c7c701e9338c8410bac9d786835dc995a09dc340b082d2e7`  
		Last Modified: Fri, 01 Mar 2024 19:35:39 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:02728f5bbdb7830b956036d0a0111d641e05b82ab319e13b5299a17c485a1970
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8502166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fac8f988153708350b39d2fa875e99657ca77ab17a7173e8a9f3e159795f0934`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Fri, 01 Mar 2024 19:29:24 GMT
ENV NATS_SERVER=2.9.25
# Fri, 01 Mar 2024 19:29:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 01 Mar 2024 19:29:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 01 Mar 2024 19:29:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 01 Mar 2024 19:29:27 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:29:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Mar 2024 19:29:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cce374196fe11964bde84ab9e7af7bb305868417e105d0fce426cc3e4308ec37`  
		Last Modified: Fri, 01 Mar 2024 19:29:59 GMT  
		Size: 5.6 MB (5599775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d6278d89313872c90d3d73d9ee9c746563d1c85be894365f21405c2dabf861`  
		Last Modified: Fri, 01 Mar 2024 19:29:58 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781a245fd1429d95c91ca449fc8de8977a259d609c8ecad513adcf3673865b25`  
		Last Modified: Fri, 01 Mar 2024 19:29:57 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:2e9ccb137222b0deb7d019f2bbe7a60a2fce2085185c822a56f3b7e991394537
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8743090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79798f50c9548f6089fb8acc7da12948f83d0941af75a8b6141101578e6f0500`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Fri, 01 Mar 2024 19:40:14 GMT
ENV NATS_SERVER=2.9.25
# Fri, 01 Mar 2024 19:40:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 01 Mar 2024 19:40:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 01 Mar 2024 19:40:16 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 01 Mar 2024 19:40:16 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:40:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Mar 2024 19:40:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454b11a8d457963acb6f066b6a05f92822390213e0d79de8b15beb1bcc8c1e7a`  
		Last Modified: Fri, 01 Mar 2024 19:40:46 GMT  
		Size: 5.4 MB (5408730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8fc2349a6c8dec4c9740388ee8a1ebe0c6c88f5496059a0c52f9d9ccedc717`  
		Last Modified: Fri, 01 Mar 2024 19:40:45 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb31da3d00d13b41bc8b2fc04330a480b934b06902d59de35519f758de40a63`  
		Last Modified: Fri, 01 Mar 2024 19:40:45 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine3.18`

```console
$ docker pull nats@sha256:aeabd56ea61bac76bfed034f6cd174ec5c67b9224d2492368cfc24909594412c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:98626a6255a2e27f6d2ddec17334d5a0046d63e0248c7a15518ebafb08598792
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9bdf51c21f823de1be2eff2f66d47cab646e69abd993ac29ce36ff1b615e95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Fri, 01 Mar 2024 19:20:36 GMT
ENV NATS_SERVER=2.9.25
# Fri, 01 Mar 2024 19:20:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 01 Mar 2024 19:20:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 01 Mar 2024 19:20:38 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 01 Mar 2024 19:20:38 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:20:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Mar 2024 19:20:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7725f62690c33c886fe27001486c543e1c50b5daf8c01573c3ab81a14c6f8d6a`  
		Last Modified: Fri, 01 Mar 2024 19:21:17 GMT  
		Size: 5.9 MB (5870706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63da9b0552d29d7213701b52a2e694569aa55262c6b47bad12863843434224b0`  
		Last Modified: Fri, 01 Mar 2024 19:21:16 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b5c9d61be8d0316e11d04da18e299abd7c27033460f7db0c3c5750e37387f6`  
		Last Modified: Fri, 01 Mar 2024 19:21:16 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:ea4229e8bb324a257fcddf953610d47ca443186fa8366ac6a5f61a9f1b4bdddd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8755242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b924a50cd5fb602a79fb5ed81445937bb67c1e9d01eb05b9ebc4ae2a5ca414a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Fri, 01 Mar 2024 19:35:07 GMT
ENV NATS_SERVER=2.9.25
# Fri, 01 Mar 2024 19:35:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 01 Mar 2024 19:35:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 01 Mar 2024 19:35:10 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 01 Mar 2024 19:35:11 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:35:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Mar 2024 19:35:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d68ec422dee341bb1f4eb7e01dec24854079424aa33eddc2d0cea72669144a`  
		Last Modified: Fri, 01 Mar 2024 19:35:40 GMT  
		Size: 5.6 MB (5607183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43baee7c50e69ffb5fb9c14225c9643a0b92cdf44a40a62a716de40b692708b1`  
		Last Modified: Fri, 01 Mar 2024 19:35:39 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e86a76ef5558f8c7c701e9338c8410bac9d786835dc995a09dc340b082d2e7`  
		Last Modified: Fri, 01 Mar 2024 19:35:39 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:02728f5bbdb7830b956036d0a0111d641e05b82ab319e13b5299a17c485a1970
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8502166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fac8f988153708350b39d2fa875e99657ca77ab17a7173e8a9f3e159795f0934`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Fri, 01 Mar 2024 19:29:24 GMT
ENV NATS_SERVER=2.9.25
# Fri, 01 Mar 2024 19:29:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 01 Mar 2024 19:29:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 01 Mar 2024 19:29:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 01 Mar 2024 19:29:27 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:29:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Mar 2024 19:29:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cce374196fe11964bde84ab9e7af7bb305868417e105d0fce426cc3e4308ec37`  
		Last Modified: Fri, 01 Mar 2024 19:29:59 GMT  
		Size: 5.6 MB (5599775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d6278d89313872c90d3d73d9ee9c746563d1c85be894365f21405c2dabf861`  
		Last Modified: Fri, 01 Mar 2024 19:29:58 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781a245fd1429d95c91ca449fc8de8977a259d609c8ecad513adcf3673865b25`  
		Last Modified: Fri, 01 Mar 2024 19:29:57 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:2e9ccb137222b0deb7d019f2bbe7a60a2fce2085185c822a56f3b7e991394537
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8743090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79798f50c9548f6089fb8acc7da12948f83d0941af75a8b6141101578e6f0500`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Fri, 01 Mar 2024 19:40:14 GMT
ENV NATS_SERVER=2.9.25
# Fri, 01 Mar 2024 19:40:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 01 Mar 2024 19:40:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 01 Mar 2024 19:40:16 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 01 Mar 2024 19:40:16 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:40:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Mar 2024 19:40:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454b11a8d457963acb6f066b6a05f92822390213e0d79de8b15beb1bcc8c1e7a`  
		Last Modified: Fri, 01 Mar 2024 19:40:46 GMT  
		Size: 5.4 MB (5408730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8fc2349a6c8dec4c9740388ee8a1ebe0c6c88f5496059a0c52f9d9ccedc717`  
		Last Modified: Fri, 01 Mar 2024 19:40:45 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb31da3d00d13b41bc8b2fc04330a480b934b06902d59de35519f758de40a63`  
		Last Modified: Fri, 01 Mar 2024 19:40:45 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-linux`

```console
$ docker pull nats@sha256:0a82ff2655b58da57640830854cc737d3d11b576feff75cfebbeba6c816a9b6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-linux` - linux; amd64

```console
$ docker pull nats@sha256:a7e4a1ba3c39879534d979369e31ec8818a48ead1ba701c582b5d6e352633504
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f668a6e8b2011067cca2504c059f26a5a7c06041892e8ba5b714d710cb9bd826`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 Mar 2024 19:20:44 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Fri, 01 Mar 2024 19:20:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 01 Mar 2024 19:20:44 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:20:45 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 Mar 2024 19:20:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f699f223b48ced53c4ba45eeb6d1ac552aa28bf511fc0df9ae5c4c3a65c971ba`  
		Last Modified: Fri, 01 Mar 2024 19:21:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:4576f0b4cb82774a99d4042d21706c0520ce243e70e3f96a060582ec8f72f6a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77c382d3556ef41f298f7d208a816a5396fd07a0d6c5760dd20b10e929d33a1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 Mar 2024 19:35:14 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Fri, 01 Mar 2024 19:35:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 01 Mar 2024 19:35:14 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:35:14 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 Mar 2024 19:35:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ac152519d53c3088e03edd635f8549e9cab54891c40718081ce170cf339d4c`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:2d00f74b5e4925e094e8c255bd54b9ba990dfbb5a8075b8deefe157ab776f6a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ef38d849c572b0ea5b33edd7fc7159a4f23e6d7ec34f61f36e9f16318289c7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 Mar 2024 19:29:31 GMT
COPY file:f989a3b6b3046a59c074559b413150c95cf8d5d1ad18593e3196fb2358872062 in /nats-server 
# Fri, 01 Mar 2024 19:29:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 01 Mar 2024 19:29:31 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:29:32 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 Mar 2024 19:29:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27bc08b69112c5d2b1303c6851c8f28dabd07a534f6cbd40dd483f3b42592d2`  
		Last Modified: Fri, 01 Mar 2024 19:30:15 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:0552a257c7e45b31aed00e37608ef4385b9714e9df68c036b6e5616d008f5fbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4786381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3c06731f019f3225f45063fe5eb50a27f4f5eab3a5f0f12b643c25a17a342f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 Mar 2024 19:40:20 GMT
COPY file:9f4f9739ea11f1ae7dd58ca32aa05c035fc77596540ec47bb5bc6d740714b029 in /nats-server 
# Fri, 01 Mar 2024 19:40:20 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 01 Mar 2024 19:40:20 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:40:20 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 Mar 2024 19:40:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee63d7485e86263b322f1514b9465e29e85b0c63a9841f6221a71833eb8dd33f`  
		Last Modified: Fri, 01 Mar 2024 19:41:00 GMT  
		Size: 4.8 MB (4785873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76ab54766965e7e61847c4162711672786e627368e813179d7fd5efa6da087b`  
		Last Modified: Fri, 01 Mar 2024 19:40:59 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver`

```console
$ docker pull nats@sha256:e15007d459fa5ed776bc89f5389519afb4ef7fe2b2fa11876bfdb61878aa47a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats:2.9-nanoserver` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats@sha256:2a0edb9c78e120898b59a4a26832b10af1b7a3313fe33636909dfbeef1cd2324
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109956305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5312bf2efd913e451ee0db83acca1f25a9eec760869c1785e7743ba150bc06`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 02:21:55 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:25:34 GMT
RUN cmd /S /C #(nop) COPY file:31589978aebc5df05c83dcc5cc9a06694b3e1d255303397414d4436e5e7f1956 in C:\nats-server.exe 
# Wed, 13 Mar 2024 02:25:35 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Mar 2024 02:25:36 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 02:25:37 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Mar 2024 02:25:37 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e772fbc90f54f9eab2951a9615b88e9eca8fc78909aba2cb3678cc214eb88ae2`  
		Last Modified: Wed, 13 Mar 2024 02:26:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48a62a905b35a3add32f2e94c895a37fdb4d62713c900f09113355b4ff6a0b58`  
		Last Modified: Wed, 13 Mar 2024 02:26:51 GMT  
		Size: 5.3 MB (5330041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab6c384ca4f265eb96264a15213fa01cce314c37d4e1fca4a886804cea0497bd`  
		Last Modified: Wed, 13 Mar 2024 02:26:49 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e8e4c880de3a51a76f4ef21996f274f0cbd4b38d894ba158d90a9cab885362`  
		Last Modified: Wed, 13 Mar 2024 02:26:50 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741736121cda315d62a64bc41c2666e9d17bd39730ab0e26fefcfba66dc918bb`  
		Last Modified: Wed, 13 Mar 2024 02:26:49 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568fc170fb79e50d824dd4e0170644cbb77cdc73aaedc47eb1fa4f6bc48e1355`  
		Last Modified: Wed, 13 Mar 2024 02:26:50 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver-1809`

```console
$ docker pull nats@sha256:e15007d459fa5ed776bc89f5389519afb4ef7fe2b2fa11876bfdb61878aa47a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats:2.9-nanoserver-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats@sha256:2a0edb9c78e120898b59a4a26832b10af1b7a3313fe33636909dfbeef1cd2324
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109956305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5312bf2efd913e451ee0db83acca1f25a9eec760869c1785e7743ba150bc06`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 02:21:55 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:25:34 GMT
RUN cmd /S /C #(nop) COPY file:31589978aebc5df05c83dcc5cc9a06694b3e1d255303397414d4436e5e7f1956 in C:\nats-server.exe 
# Wed, 13 Mar 2024 02:25:35 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Mar 2024 02:25:36 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 02:25:37 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Mar 2024 02:25:37 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e772fbc90f54f9eab2951a9615b88e9eca8fc78909aba2cb3678cc214eb88ae2`  
		Last Modified: Wed, 13 Mar 2024 02:26:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48a62a905b35a3add32f2e94c895a37fdb4d62713c900f09113355b4ff6a0b58`  
		Last Modified: Wed, 13 Mar 2024 02:26:51 GMT  
		Size: 5.3 MB (5330041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab6c384ca4f265eb96264a15213fa01cce314c37d4e1fca4a886804cea0497bd`  
		Last Modified: Wed, 13 Mar 2024 02:26:49 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e8e4c880de3a51a76f4ef21996f274f0cbd4b38d894ba158d90a9cab885362`  
		Last Modified: Wed, 13 Mar 2024 02:26:50 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741736121cda315d62a64bc41c2666e9d17bd39730ab0e26fefcfba66dc918bb`  
		Last Modified: Wed, 13 Mar 2024 02:26:49 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568fc170fb79e50d824dd4e0170644cbb77cdc73aaedc47eb1fa4f6bc48e1355`  
		Last Modified: Wed, 13 Mar 2024 02:26:50 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-scratch`

```console
$ docker pull nats@sha256:0a82ff2655b58da57640830854cc737d3d11b576feff75cfebbeba6c816a9b6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-scratch` - linux; amd64

```console
$ docker pull nats@sha256:a7e4a1ba3c39879534d979369e31ec8818a48ead1ba701c582b5d6e352633504
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f668a6e8b2011067cca2504c059f26a5a7c06041892e8ba5b714d710cb9bd826`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 Mar 2024 19:20:44 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Fri, 01 Mar 2024 19:20:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 01 Mar 2024 19:20:44 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:20:45 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 Mar 2024 19:20:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f699f223b48ced53c4ba45eeb6d1ac552aa28bf511fc0df9ae5c4c3a65c971ba`  
		Last Modified: Fri, 01 Mar 2024 19:21:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:4576f0b4cb82774a99d4042d21706c0520ce243e70e3f96a060582ec8f72f6a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77c382d3556ef41f298f7d208a816a5396fd07a0d6c5760dd20b10e929d33a1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 Mar 2024 19:35:14 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Fri, 01 Mar 2024 19:35:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 01 Mar 2024 19:35:14 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:35:14 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 Mar 2024 19:35:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ac152519d53c3088e03edd635f8549e9cab54891c40718081ce170cf339d4c`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:2d00f74b5e4925e094e8c255bd54b9ba990dfbb5a8075b8deefe157ab776f6a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ef38d849c572b0ea5b33edd7fc7159a4f23e6d7ec34f61f36e9f16318289c7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 Mar 2024 19:29:31 GMT
COPY file:f989a3b6b3046a59c074559b413150c95cf8d5d1ad18593e3196fb2358872062 in /nats-server 
# Fri, 01 Mar 2024 19:29:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 01 Mar 2024 19:29:31 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:29:32 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 Mar 2024 19:29:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27bc08b69112c5d2b1303c6851c8f28dabd07a534f6cbd40dd483f3b42592d2`  
		Last Modified: Fri, 01 Mar 2024 19:30:15 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:0552a257c7e45b31aed00e37608ef4385b9714e9df68c036b6e5616d008f5fbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4786381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3c06731f019f3225f45063fe5eb50a27f4f5eab3a5f0f12b643c25a17a342f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 Mar 2024 19:40:20 GMT
COPY file:9f4f9739ea11f1ae7dd58ca32aa05c035fc77596540ec47bb5bc6d740714b029 in /nats-server 
# Fri, 01 Mar 2024 19:40:20 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 01 Mar 2024 19:40:20 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:40:20 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 Mar 2024 19:40:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee63d7485e86263b322f1514b9465e29e85b0c63a9841f6221a71833eb8dd33f`  
		Last Modified: Fri, 01 Mar 2024 19:41:00 GMT  
		Size: 4.8 MB (4785873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76ab54766965e7e61847c4162711672786e627368e813179d7fd5efa6da087b`  
		Last Modified: Fri, 01 Mar 2024 19:40:59 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore`

```console
$ docker pull nats@sha256:bd8de4cfd5b2fda3b1ad96359083d7f52a21d53ef70b527e1b8b556ca4c2a898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats:2.9-windowsservercore` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats@sha256:30b29fc5d995af5948b03ff5486f2f5feeac859297a76af49e83e3f78ca122f1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2131213705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7621d3b516b8026558648b447a29731cc16a2743605e28cf9c6a2762ecffc9b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 02:18:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Mar 2024 02:18:28 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:22:05 GMT
ENV NATS_SERVER=2.9.25
# Wed, 13 Mar 2024 02:22:06 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.25/nats-server-v2.9.25-windows-amd64.zip
# Wed, 13 Mar 2024 02:22:07 GMT
ENV NATS_SERVER_SHASUM=7cebcf3487ebeae9ab66e2af8a99ce891d78357bb9325de95d1c38bbf5c647a2
# Wed, 13 Mar 2024 02:23:24 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Mar 2024 02:25:11 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 13 Mar 2024 02:25:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Mar 2024 02:25:12 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 02:25:13 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Mar 2024 02:25:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e169e85f3c664d99b16235c550eb744e7e1421ceb3b4a239fd727321ccddc77`  
		Last Modified: Wed, 13 Mar 2024 02:26:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7cb8b6faf23b1820a39bd95d7664a27dd6143342b384e0331e51b7e7ba82b72`  
		Last Modified: Wed, 13 Mar 2024 02:26:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e2b92ebd4a717c111621c029962f2810658458c56b83348cd48ebaa4fe3068b`  
		Last Modified: Wed, 13 Mar 2024 02:26:41 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6530379ce7a04a762f33d3d224a027ad212974c8a0655010b0d6a64bc7b85c7a`  
		Last Modified: Wed, 13 Mar 2024 02:26:41 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f26449b202b587050f84dcbf4d1f5a6c2781a3ec496544a734a1c5aa6f84a47`  
		Last Modified: Wed, 13 Mar 2024 02:26:41 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b10fec8d5c8ffdc42af4071313da5e34d583a3354402e2292272981753aefd`  
		Last Modified: Wed, 13 Mar 2024 02:26:41 GMT  
		Size: 464.4 KB (464409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a24c99d6622471210ace9816e54ba35306060d852b8066456f0709d0d0a91169`  
		Last Modified: Wed, 13 Mar 2024 02:26:40 GMT  
		Size: 5.6 MB (5636561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e7f775a4d40bc0c3366839ccfff3892ca055cc7ff193756fcfebf651992727`  
		Last Modified: Wed, 13 Mar 2024 02:26:39 GMT  
		Size: 1.9 KB (1863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12930ef98a4996768cfcb1ca318dbb40c5b8fdb11e481ed1252b2bef55b83e13`  
		Last Modified: Wed, 13 Mar 2024 02:26:39 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a24b35dc5b5c0fe780138a63f9518dcebf4b9472677f95c385a5768e6139e11`  
		Last Modified: Wed, 13 Mar 2024 02:26:39 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ef9209ec4c451a237994ffe079fdb41815c69eed7e68bc677b80efd12710c2`  
		Last Modified: Wed, 13 Mar 2024 02:26:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore-1809`

```console
$ docker pull nats@sha256:bd8de4cfd5b2fda3b1ad96359083d7f52a21d53ef70b527e1b8b556ca4c2a898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats:2.9-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats@sha256:30b29fc5d995af5948b03ff5486f2f5feeac859297a76af49e83e3f78ca122f1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2131213705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7621d3b516b8026558648b447a29731cc16a2743605e28cf9c6a2762ecffc9b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 02:18:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Mar 2024 02:18:28 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:22:05 GMT
ENV NATS_SERVER=2.9.25
# Wed, 13 Mar 2024 02:22:06 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.25/nats-server-v2.9.25-windows-amd64.zip
# Wed, 13 Mar 2024 02:22:07 GMT
ENV NATS_SERVER_SHASUM=7cebcf3487ebeae9ab66e2af8a99ce891d78357bb9325de95d1c38bbf5c647a2
# Wed, 13 Mar 2024 02:23:24 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Mar 2024 02:25:11 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 13 Mar 2024 02:25:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Mar 2024 02:25:12 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 02:25:13 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Mar 2024 02:25:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e169e85f3c664d99b16235c550eb744e7e1421ceb3b4a239fd727321ccddc77`  
		Last Modified: Wed, 13 Mar 2024 02:26:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7cb8b6faf23b1820a39bd95d7664a27dd6143342b384e0331e51b7e7ba82b72`  
		Last Modified: Wed, 13 Mar 2024 02:26:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e2b92ebd4a717c111621c029962f2810658458c56b83348cd48ebaa4fe3068b`  
		Last Modified: Wed, 13 Mar 2024 02:26:41 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6530379ce7a04a762f33d3d224a027ad212974c8a0655010b0d6a64bc7b85c7a`  
		Last Modified: Wed, 13 Mar 2024 02:26:41 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f26449b202b587050f84dcbf4d1f5a6c2781a3ec496544a734a1c5aa6f84a47`  
		Last Modified: Wed, 13 Mar 2024 02:26:41 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b10fec8d5c8ffdc42af4071313da5e34d583a3354402e2292272981753aefd`  
		Last Modified: Wed, 13 Mar 2024 02:26:41 GMT  
		Size: 464.4 KB (464409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a24c99d6622471210ace9816e54ba35306060d852b8066456f0709d0d0a91169`  
		Last Modified: Wed, 13 Mar 2024 02:26:40 GMT  
		Size: 5.6 MB (5636561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e7f775a4d40bc0c3366839ccfff3892ca055cc7ff193756fcfebf651992727`  
		Last Modified: Wed, 13 Mar 2024 02:26:39 GMT  
		Size: 1.9 KB (1863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12930ef98a4996768cfcb1ca318dbb40c5b8fdb11e481ed1252b2bef55b83e13`  
		Last Modified: Wed, 13 Mar 2024 02:26:39 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a24b35dc5b5c0fe780138a63f9518dcebf4b9472677f95c385a5768e6139e11`  
		Last Modified: Wed, 13 Mar 2024 02:26:39 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ef9209ec4c451a237994ffe079fdb41815c69eed7e68bc677b80efd12710c2`  
		Last Modified: Wed, 13 Mar 2024 02:26:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25`

```console
$ docker pull nats@sha256:0a82ff2655b58da57640830854cc737d3d11b576feff75cfebbeba6c816a9b6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.25` - linux; amd64

```console
$ docker pull nats@sha256:a7e4a1ba3c39879534d979369e31ec8818a48ead1ba701c582b5d6e352633504
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f668a6e8b2011067cca2504c059f26a5a7c06041892e8ba5b714d710cb9bd826`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 Mar 2024 19:20:44 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Fri, 01 Mar 2024 19:20:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 01 Mar 2024 19:20:44 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:20:45 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 Mar 2024 19:20:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f699f223b48ced53c4ba45eeb6d1ac552aa28bf511fc0df9ae5c4c3a65c971ba`  
		Last Modified: Fri, 01 Mar 2024 19:21:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25` - linux; arm variant v6

```console
$ docker pull nats@sha256:4576f0b4cb82774a99d4042d21706c0520ce243e70e3f96a060582ec8f72f6a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77c382d3556ef41f298f7d208a816a5396fd07a0d6c5760dd20b10e929d33a1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 Mar 2024 19:35:14 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Fri, 01 Mar 2024 19:35:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 01 Mar 2024 19:35:14 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:35:14 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 Mar 2024 19:35:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ac152519d53c3088e03edd635f8549e9cab54891c40718081ce170cf339d4c`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25` - linux; arm variant v7

```console
$ docker pull nats@sha256:2d00f74b5e4925e094e8c255bd54b9ba990dfbb5a8075b8deefe157ab776f6a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ef38d849c572b0ea5b33edd7fc7159a4f23e6d7ec34f61f36e9f16318289c7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 Mar 2024 19:29:31 GMT
COPY file:f989a3b6b3046a59c074559b413150c95cf8d5d1ad18593e3196fb2358872062 in /nats-server 
# Fri, 01 Mar 2024 19:29:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 01 Mar 2024 19:29:31 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:29:32 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 Mar 2024 19:29:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27bc08b69112c5d2b1303c6851c8f28dabd07a534f6cbd40dd483f3b42592d2`  
		Last Modified: Fri, 01 Mar 2024 19:30:15 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:0552a257c7e45b31aed00e37608ef4385b9714e9df68c036b6e5616d008f5fbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4786381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3c06731f019f3225f45063fe5eb50a27f4f5eab3a5f0f12b643c25a17a342f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 Mar 2024 19:40:20 GMT
COPY file:9f4f9739ea11f1ae7dd58ca32aa05c035fc77596540ec47bb5bc6d740714b029 in /nats-server 
# Fri, 01 Mar 2024 19:40:20 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 01 Mar 2024 19:40:20 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:40:20 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 Mar 2024 19:40:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee63d7485e86263b322f1514b9465e29e85b0c63a9841f6221a71833eb8dd33f`  
		Last Modified: Fri, 01 Mar 2024 19:41:00 GMT  
		Size: 4.8 MB (4785873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76ab54766965e7e61847c4162711672786e627368e813179d7fd5efa6da087b`  
		Last Modified: Fri, 01 Mar 2024 19:40:59 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-alpine`

```console
$ docker pull nats@sha256:aeabd56ea61bac76bfed034f6cd174ec5c67b9224d2492368cfc24909594412c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.25-alpine` - linux; amd64

```console
$ docker pull nats@sha256:98626a6255a2e27f6d2ddec17334d5a0046d63e0248c7a15518ebafb08598792
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9bdf51c21f823de1be2eff2f66d47cab646e69abd993ac29ce36ff1b615e95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Fri, 01 Mar 2024 19:20:36 GMT
ENV NATS_SERVER=2.9.25
# Fri, 01 Mar 2024 19:20:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 01 Mar 2024 19:20:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 01 Mar 2024 19:20:38 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 01 Mar 2024 19:20:38 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:20:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Mar 2024 19:20:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7725f62690c33c886fe27001486c543e1c50b5daf8c01573c3ab81a14c6f8d6a`  
		Last Modified: Fri, 01 Mar 2024 19:21:17 GMT  
		Size: 5.9 MB (5870706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63da9b0552d29d7213701b52a2e694569aa55262c6b47bad12863843434224b0`  
		Last Modified: Fri, 01 Mar 2024 19:21:16 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b5c9d61be8d0316e11d04da18e299abd7c27033460f7db0c3c5750e37387f6`  
		Last Modified: Fri, 01 Mar 2024 19:21:16 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:ea4229e8bb324a257fcddf953610d47ca443186fa8366ac6a5f61a9f1b4bdddd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8755242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b924a50cd5fb602a79fb5ed81445937bb67c1e9d01eb05b9ebc4ae2a5ca414a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Fri, 01 Mar 2024 19:35:07 GMT
ENV NATS_SERVER=2.9.25
# Fri, 01 Mar 2024 19:35:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 01 Mar 2024 19:35:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 01 Mar 2024 19:35:10 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 01 Mar 2024 19:35:11 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:35:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Mar 2024 19:35:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d68ec422dee341bb1f4eb7e01dec24854079424aa33eddc2d0cea72669144a`  
		Last Modified: Fri, 01 Mar 2024 19:35:40 GMT  
		Size: 5.6 MB (5607183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43baee7c50e69ffb5fb9c14225c9643a0b92cdf44a40a62a716de40b692708b1`  
		Last Modified: Fri, 01 Mar 2024 19:35:39 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e86a76ef5558f8c7c701e9338c8410bac9d786835dc995a09dc340b082d2e7`  
		Last Modified: Fri, 01 Mar 2024 19:35:39 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:02728f5bbdb7830b956036d0a0111d641e05b82ab319e13b5299a17c485a1970
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8502166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fac8f988153708350b39d2fa875e99657ca77ab17a7173e8a9f3e159795f0934`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Fri, 01 Mar 2024 19:29:24 GMT
ENV NATS_SERVER=2.9.25
# Fri, 01 Mar 2024 19:29:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 01 Mar 2024 19:29:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 01 Mar 2024 19:29:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 01 Mar 2024 19:29:27 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:29:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Mar 2024 19:29:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cce374196fe11964bde84ab9e7af7bb305868417e105d0fce426cc3e4308ec37`  
		Last Modified: Fri, 01 Mar 2024 19:29:59 GMT  
		Size: 5.6 MB (5599775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d6278d89313872c90d3d73d9ee9c746563d1c85be894365f21405c2dabf861`  
		Last Modified: Fri, 01 Mar 2024 19:29:58 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781a245fd1429d95c91ca449fc8de8977a259d609c8ecad513adcf3673865b25`  
		Last Modified: Fri, 01 Mar 2024 19:29:57 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:2e9ccb137222b0deb7d019f2bbe7a60a2fce2085185c822a56f3b7e991394537
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8743090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79798f50c9548f6089fb8acc7da12948f83d0941af75a8b6141101578e6f0500`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Fri, 01 Mar 2024 19:40:14 GMT
ENV NATS_SERVER=2.9.25
# Fri, 01 Mar 2024 19:40:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 01 Mar 2024 19:40:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 01 Mar 2024 19:40:16 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 01 Mar 2024 19:40:16 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:40:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Mar 2024 19:40:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454b11a8d457963acb6f066b6a05f92822390213e0d79de8b15beb1bcc8c1e7a`  
		Last Modified: Fri, 01 Mar 2024 19:40:46 GMT  
		Size: 5.4 MB (5408730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8fc2349a6c8dec4c9740388ee8a1ebe0c6c88f5496059a0c52f9d9ccedc717`  
		Last Modified: Fri, 01 Mar 2024 19:40:45 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb31da3d00d13b41bc8b2fc04330a480b934b06902d59de35519f758de40a63`  
		Last Modified: Fri, 01 Mar 2024 19:40:45 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-alpine3.18`

```console
$ docker pull nats@sha256:aeabd56ea61bac76bfed034f6cd174ec5c67b9224d2492368cfc24909594412c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.25-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:98626a6255a2e27f6d2ddec17334d5a0046d63e0248c7a15518ebafb08598792
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9bdf51c21f823de1be2eff2f66d47cab646e69abd993ac29ce36ff1b615e95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Fri, 01 Mar 2024 19:20:36 GMT
ENV NATS_SERVER=2.9.25
# Fri, 01 Mar 2024 19:20:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 01 Mar 2024 19:20:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 01 Mar 2024 19:20:38 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 01 Mar 2024 19:20:38 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:20:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Mar 2024 19:20:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7725f62690c33c886fe27001486c543e1c50b5daf8c01573c3ab81a14c6f8d6a`  
		Last Modified: Fri, 01 Mar 2024 19:21:17 GMT  
		Size: 5.9 MB (5870706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63da9b0552d29d7213701b52a2e694569aa55262c6b47bad12863843434224b0`  
		Last Modified: Fri, 01 Mar 2024 19:21:16 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b5c9d61be8d0316e11d04da18e299abd7c27033460f7db0c3c5750e37387f6`  
		Last Modified: Fri, 01 Mar 2024 19:21:16 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:ea4229e8bb324a257fcddf953610d47ca443186fa8366ac6a5f61a9f1b4bdddd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8755242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b924a50cd5fb602a79fb5ed81445937bb67c1e9d01eb05b9ebc4ae2a5ca414a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Fri, 01 Mar 2024 19:35:07 GMT
ENV NATS_SERVER=2.9.25
# Fri, 01 Mar 2024 19:35:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 01 Mar 2024 19:35:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 01 Mar 2024 19:35:10 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 01 Mar 2024 19:35:11 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:35:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Mar 2024 19:35:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d68ec422dee341bb1f4eb7e01dec24854079424aa33eddc2d0cea72669144a`  
		Last Modified: Fri, 01 Mar 2024 19:35:40 GMT  
		Size: 5.6 MB (5607183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43baee7c50e69ffb5fb9c14225c9643a0b92cdf44a40a62a716de40b692708b1`  
		Last Modified: Fri, 01 Mar 2024 19:35:39 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e86a76ef5558f8c7c701e9338c8410bac9d786835dc995a09dc340b082d2e7`  
		Last Modified: Fri, 01 Mar 2024 19:35:39 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:02728f5bbdb7830b956036d0a0111d641e05b82ab319e13b5299a17c485a1970
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8502166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fac8f988153708350b39d2fa875e99657ca77ab17a7173e8a9f3e159795f0934`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Fri, 01 Mar 2024 19:29:24 GMT
ENV NATS_SERVER=2.9.25
# Fri, 01 Mar 2024 19:29:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 01 Mar 2024 19:29:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 01 Mar 2024 19:29:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 01 Mar 2024 19:29:27 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:29:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Mar 2024 19:29:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cce374196fe11964bde84ab9e7af7bb305868417e105d0fce426cc3e4308ec37`  
		Last Modified: Fri, 01 Mar 2024 19:29:59 GMT  
		Size: 5.6 MB (5599775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d6278d89313872c90d3d73d9ee9c746563d1c85be894365f21405c2dabf861`  
		Last Modified: Fri, 01 Mar 2024 19:29:58 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781a245fd1429d95c91ca449fc8de8977a259d609c8ecad513adcf3673865b25`  
		Last Modified: Fri, 01 Mar 2024 19:29:57 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:2e9ccb137222b0deb7d019f2bbe7a60a2fce2085185c822a56f3b7e991394537
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8743090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79798f50c9548f6089fb8acc7da12948f83d0941af75a8b6141101578e6f0500`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Fri, 01 Mar 2024 19:40:14 GMT
ENV NATS_SERVER=2.9.25
# Fri, 01 Mar 2024 19:40:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='68551379667a0caffc5c5302f817b99b89c133077ca84b2cf72e1947a46e0e9e' ;; 		armhf) natsArch='arm6'; sha256='e6b591717c7d4401fa5c9cbefa2891884bebed60c7bcfe874ebbeef00134c146' ;; 		armv7) natsArch='arm7'; sha256='b0c01674252e2e01fd50492af954797427db63acfcffb026911735e38612f493' ;; 		x86_64) natsArch='amd64'; sha256='2da5e9ba29ec29a5e44775c1cfe8ade6e3506606b4b361276dfd8a08f273da99' ;; 		x86) natsArch='386'; sha256='35260af09fe2039bdedc6bc258c823cdca09929e9c6003faf5d16a6f28c44c32' ;; 		s390x) natsArch='s390x'; sha256='e1d2b0079dc0a7a13509dc34e371bab9824b90a1c816a21a9f153b2482dac08c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 01 Mar 2024 19:40:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 01 Mar 2024 19:40:16 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 01 Mar 2024 19:40:16 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:40:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Mar 2024 19:40:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454b11a8d457963acb6f066b6a05f92822390213e0d79de8b15beb1bcc8c1e7a`  
		Last Modified: Fri, 01 Mar 2024 19:40:46 GMT  
		Size: 5.4 MB (5408730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8fc2349a6c8dec4c9740388ee8a1ebe0c6c88f5496059a0c52f9d9ccedc717`  
		Last Modified: Fri, 01 Mar 2024 19:40:45 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb31da3d00d13b41bc8b2fc04330a480b934b06902d59de35519f758de40a63`  
		Last Modified: Fri, 01 Mar 2024 19:40:45 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-linux`

```console
$ docker pull nats@sha256:0a82ff2655b58da57640830854cc737d3d11b576feff75cfebbeba6c816a9b6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.25-linux` - linux; amd64

```console
$ docker pull nats@sha256:a7e4a1ba3c39879534d979369e31ec8818a48ead1ba701c582b5d6e352633504
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f668a6e8b2011067cca2504c059f26a5a7c06041892e8ba5b714d710cb9bd826`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 Mar 2024 19:20:44 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Fri, 01 Mar 2024 19:20:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 01 Mar 2024 19:20:44 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:20:45 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 Mar 2024 19:20:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f699f223b48ced53c4ba45eeb6d1ac552aa28bf511fc0df9ae5c4c3a65c971ba`  
		Last Modified: Fri, 01 Mar 2024 19:21:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:4576f0b4cb82774a99d4042d21706c0520ce243e70e3f96a060582ec8f72f6a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77c382d3556ef41f298f7d208a816a5396fd07a0d6c5760dd20b10e929d33a1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 Mar 2024 19:35:14 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Fri, 01 Mar 2024 19:35:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 01 Mar 2024 19:35:14 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:35:14 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 Mar 2024 19:35:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ac152519d53c3088e03edd635f8549e9cab54891c40718081ce170cf339d4c`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:2d00f74b5e4925e094e8c255bd54b9ba990dfbb5a8075b8deefe157ab776f6a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ef38d849c572b0ea5b33edd7fc7159a4f23e6d7ec34f61f36e9f16318289c7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 Mar 2024 19:29:31 GMT
COPY file:f989a3b6b3046a59c074559b413150c95cf8d5d1ad18593e3196fb2358872062 in /nats-server 
# Fri, 01 Mar 2024 19:29:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 01 Mar 2024 19:29:31 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:29:32 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 Mar 2024 19:29:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27bc08b69112c5d2b1303c6851c8f28dabd07a534f6cbd40dd483f3b42592d2`  
		Last Modified: Fri, 01 Mar 2024 19:30:15 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:0552a257c7e45b31aed00e37608ef4385b9714e9df68c036b6e5616d008f5fbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4786381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3c06731f019f3225f45063fe5eb50a27f4f5eab3a5f0f12b643c25a17a342f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 Mar 2024 19:40:20 GMT
COPY file:9f4f9739ea11f1ae7dd58ca32aa05c035fc77596540ec47bb5bc6d740714b029 in /nats-server 
# Fri, 01 Mar 2024 19:40:20 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 01 Mar 2024 19:40:20 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:40:20 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 Mar 2024 19:40:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee63d7485e86263b322f1514b9465e29e85b0c63a9841f6221a71833eb8dd33f`  
		Last Modified: Fri, 01 Mar 2024 19:41:00 GMT  
		Size: 4.8 MB (4785873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76ab54766965e7e61847c4162711672786e627368e813179d7fd5efa6da087b`  
		Last Modified: Fri, 01 Mar 2024 19:40:59 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-nanoserver`

```console
$ docker pull nats@sha256:e15007d459fa5ed776bc89f5389519afb4ef7fe2b2fa11876bfdb61878aa47a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats:2.9.25-nanoserver` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats@sha256:2a0edb9c78e120898b59a4a26832b10af1b7a3313fe33636909dfbeef1cd2324
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109956305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5312bf2efd913e451ee0db83acca1f25a9eec760869c1785e7743ba150bc06`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 02:21:55 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:25:34 GMT
RUN cmd /S /C #(nop) COPY file:31589978aebc5df05c83dcc5cc9a06694b3e1d255303397414d4436e5e7f1956 in C:\nats-server.exe 
# Wed, 13 Mar 2024 02:25:35 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Mar 2024 02:25:36 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 02:25:37 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Mar 2024 02:25:37 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e772fbc90f54f9eab2951a9615b88e9eca8fc78909aba2cb3678cc214eb88ae2`  
		Last Modified: Wed, 13 Mar 2024 02:26:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48a62a905b35a3add32f2e94c895a37fdb4d62713c900f09113355b4ff6a0b58`  
		Last Modified: Wed, 13 Mar 2024 02:26:51 GMT  
		Size: 5.3 MB (5330041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab6c384ca4f265eb96264a15213fa01cce314c37d4e1fca4a886804cea0497bd`  
		Last Modified: Wed, 13 Mar 2024 02:26:49 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e8e4c880de3a51a76f4ef21996f274f0cbd4b38d894ba158d90a9cab885362`  
		Last Modified: Wed, 13 Mar 2024 02:26:50 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741736121cda315d62a64bc41c2666e9d17bd39730ab0e26fefcfba66dc918bb`  
		Last Modified: Wed, 13 Mar 2024 02:26:49 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568fc170fb79e50d824dd4e0170644cbb77cdc73aaedc47eb1fa4f6bc48e1355`  
		Last Modified: Wed, 13 Mar 2024 02:26:50 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-nanoserver-1809`

```console
$ docker pull nats@sha256:e15007d459fa5ed776bc89f5389519afb4ef7fe2b2fa11876bfdb61878aa47a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats:2.9.25-nanoserver-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats@sha256:2a0edb9c78e120898b59a4a26832b10af1b7a3313fe33636909dfbeef1cd2324
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109956305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5312bf2efd913e451ee0db83acca1f25a9eec760869c1785e7743ba150bc06`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 02:21:55 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:25:34 GMT
RUN cmd /S /C #(nop) COPY file:31589978aebc5df05c83dcc5cc9a06694b3e1d255303397414d4436e5e7f1956 in C:\nats-server.exe 
# Wed, 13 Mar 2024 02:25:35 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Mar 2024 02:25:36 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 02:25:37 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Mar 2024 02:25:37 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e772fbc90f54f9eab2951a9615b88e9eca8fc78909aba2cb3678cc214eb88ae2`  
		Last Modified: Wed, 13 Mar 2024 02:26:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48a62a905b35a3add32f2e94c895a37fdb4d62713c900f09113355b4ff6a0b58`  
		Last Modified: Wed, 13 Mar 2024 02:26:51 GMT  
		Size: 5.3 MB (5330041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab6c384ca4f265eb96264a15213fa01cce314c37d4e1fca4a886804cea0497bd`  
		Last Modified: Wed, 13 Mar 2024 02:26:49 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e8e4c880de3a51a76f4ef21996f274f0cbd4b38d894ba158d90a9cab885362`  
		Last Modified: Wed, 13 Mar 2024 02:26:50 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741736121cda315d62a64bc41c2666e9d17bd39730ab0e26fefcfba66dc918bb`  
		Last Modified: Wed, 13 Mar 2024 02:26:49 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568fc170fb79e50d824dd4e0170644cbb77cdc73aaedc47eb1fa4f6bc48e1355`  
		Last Modified: Wed, 13 Mar 2024 02:26:50 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-scratch`

```console
$ docker pull nats@sha256:0a82ff2655b58da57640830854cc737d3d11b576feff75cfebbeba6c816a9b6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.25-scratch` - linux; amd64

```console
$ docker pull nats@sha256:a7e4a1ba3c39879534d979369e31ec8818a48ead1ba701c582b5d6e352633504
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f668a6e8b2011067cca2504c059f26a5a7c06041892e8ba5b714d710cb9bd826`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 Mar 2024 19:20:44 GMT
COPY file:e1d13d8f0578aaf77846bfea9c520b17c6332aa0bc1b3d829f5d13a550b88fcb in /nats-server 
# Fri, 01 Mar 2024 19:20:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 01 Mar 2024 19:20:44 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:20:45 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 Mar 2024 19:20:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1fa1f296a849bb1aed8b2bea50bb8eeae63669f16f238be8315c6d871cb0ff3a`  
		Last Modified: Fri, 01 Mar 2024 19:21:31 GMT  
		Size: 5.2 MB (5249058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f699f223b48ced53c4ba45eeb6d1ac552aa28bf511fc0df9ae5c4c3a65c971ba`  
		Last Modified: Fri, 01 Mar 2024 19:21:30 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:4576f0b4cb82774a99d4042d21706c0520ce243e70e3f96a060582ec8f72f6a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4986067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77c382d3556ef41f298f7d208a816a5396fd07a0d6c5760dd20b10e929d33a1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 Mar 2024 19:35:14 GMT
COPY file:69e58402303893c8fde94c7dae0e411d29d9e9c676a5f9b36c8c2f6ca23655eb in /nats-server 
# Fri, 01 Mar 2024 19:35:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 01 Mar 2024 19:35:14 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:35:14 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 Mar 2024 19:35:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27b5623a1024732949fa4f120eb4c0d315cc46cf0e684796c0f1eceede508141`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 5.0 MB (4985559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ac152519d53c3088e03edd635f8549e9cab54891c40718081ce170cf339d4c`  
		Last Modified: Fri, 01 Mar 2024 19:35:57 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:2d00f74b5e4925e094e8c255bd54b9ba990dfbb5a8075b8deefe157ab776f6a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ef38d849c572b0ea5b33edd7fc7159a4f23e6d7ec34f61f36e9f16318289c7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 Mar 2024 19:29:31 GMT
COPY file:f989a3b6b3046a59c074559b413150c95cf8d5d1ad18593e3196fb2358872062 in /nats-server 
# Fri, 01 Mar 2024 19:29:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 01 Mar 2024 19:29:31 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:29:32 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 Mar 2024 19:29:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5630b213121e73c1f5701c46495c8e65195a21cd10fffb96173f1986df54c97c`  
		Last Modified: Fri, 01 Mar 2024 19:30:21 GMT  
		Size: 5.0 MB (4978903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27bc08b69112c5d2b1303c6851c8f28dabd07a534f6cbd40dd483f3b42592d2`  
		Last Modified: Fri, 01 Mar 2024 19:30:15 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.25-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:0552a257c7e45b31aed00e37608ef4385b9714e9df68c036b6e5616d008f5fbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4786381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3c06731f019f3225f45063fe5eb50a27f4f5eab3a5f0f12b643c25a17a342f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 Mar 2024 19:40:20 GMT
COPY file:9f4f9739ea11f1ae7dd58ca32aa05c035fc77596540ec47bb5bc6d740714b029 in /nats-server 
# Fri, 01 Mar 2024 19:40:20 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 01 Mar 2024 19:40:20 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Mar 2024 19:40:20 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 Mar 2024 19:40:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee63d7485e86263b322f1514b9465e29e85b0c63a9841f6221a71833eb8dd33f`  
		Last Modified: Fri, 01 Mar 2024 19:41:00 GMT  
		Size: 4.8 MB (4785873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76ab54766965e7e61847c4162711672786e627368e813179d7fd5efa6da087b`  
		Last Modified: Fri, 01 Mar 2024 19:40:59 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-windowsservercore`

```console
$ docker pull nats@sha256:bd8de4cfd5b2fda3b1ad96359083d7f52a21d53ef70b527e1b8b556ca4c2a898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats:2.9.25-windowsservercore` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats@sha256:30b29fc5d995af5948b03ff5486f2f5feeac859297a76af49e83e3f78ca122f1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2131213705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7621d3b516b8026558648b447a29731cc16a2743605e28cf9c6a2762ecffc9b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 02:18:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Mar 2024 02:18:28 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:22:05 GMT
ENV NATS_SERVER=2.9.25
# Wed, 13 Mar 2024 02:22:06 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.25/nats-server-v2.9.25-windows-amd64.zip
# Wed, 13 Mar 2024 02:22:07 GMT
ENV NATS_SERVER_SHASUM=7cebcf3487ebeae9ab66e2af8a99ce891d78357bb9325de95d1c38bbf5c647a2
# Wed, 13 Mar 2024 02:23:24 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Mar 2024 02:25:11 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 13 Mar 2024 02:25:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Mar 2024 02:25:12 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 02:25:13 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Mar 2024 02:25:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e169e85f3c664d99b16235c550eb744e7e1421ceb3b4a239fd727321ccddc77`  
		Last Modified: Wed, 13 Mar 2024 02:26:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7cb8b6faf23b1820a39bd95d7664a27dd6143342b384e0331e51b7e7ba82b72`  
		Last Modified: Wed, 13 Mar 2024 02:26:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e2b92ebd4a717c111621c029962f2810658458c56b83348cd48ebaa4fe3068b`  
		Last Modified: Wed, 13 Mar 2024 02:26:41 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6530379ce7a04a762f33d3d224a027ad212974c8a0655010b0d6a64bc7b85c7a`  
		Last Modified: Wed, 13 Mar 2024 02:26:41 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f26449b202b587050f84dcbf4d1f5a6c2781a3ec496544a734a1c5aa6f84a47`  
		Last Modified: Wed, 13 Mar 2024 02:26:41 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b10fec8d5c8ffdc42af4071313da5e34d583a3354402e2292272981753aefd`  
		Last Modified: Wed, 13 Mar 2024 02:26:41 GMT  
		Size: 464.4 KB (464409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a24c99d6622471210ace9816e54ba35306060d852b8066456f0709d0d0a91169`  
		Last Modified: Wed, 13 Mar 2024 02:26:40 GMT  
		Size: 5.6 MB (5636561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e7f775a4d40bc0c3366839ccfff3892ca055cc7ff193756fcfebf651992727`  
		Last Modified: Wed, 13 Mar 2024 02:26:39 GMT  
		Size: 1.9 KB (1863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12930ef98a4996768cfcb1ca318dbb40c5b8fdb11e481ed1252b2bef55b83e13`  
		Last Modified: Wed, 13 Mar 2024 02:26:39 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a24b35dc5b5c0fe780138a63f9518dcebf4b9472677f95c385a5768e6139e11`  
		Last Modified: Wed, 13 Mar 2024 02:26:39 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ef9209ec4c451a237994ffe079fdb41815c69eed7e68bc677b80efd12710c2`  
		Last Modified: Wed, 13 Mar 2024 02:26:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.25-windowsservercore-1809`

```console
$ docker pull nats@sha256:bd8de4cfd5b2fda3b1ad96359083d7f52a21d53ef70b527e1b8b556ca4c2a898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats:2.9.25-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats@sha256:30b29fc5d995af5948b03ff5486f2f5feeac859297a76af49e83e3f78ca122f1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2131213705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7621d3b516b8026558648b447a29731cc16a2743605e28cf9c6a2762ecffc9b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 02:18:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Mar 2024 02:18:28 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:22:05 GMT
ENV NATS_SERVER=2.9.25
# Wed, 13 Mar 2024 02:22:06 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.25/nats-server-v2.9.25-windows-amd64.zip
# Wed, 13 Mar 2024 02:22:07 GMT
ENV NATS_SERVER_SHASUM=7cebcf3487ebeae9ab66e2af8a99ce891d78357bb9325de95d1c38bbf5c647a2
# Wed, 13 Mar 2024 02:23:24 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Mar 2024 02:25:11 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 13 Mar 2024 02:25:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Mar 2024 02:25:12 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 02:25:13 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Mar 2024 02:25:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e169e85f3c664d99b16235c550eb744e7e1421ceb3b4a239fd727321ccddc77`  
		Last Modified: Wed, 13 Mar 2024 02:26:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7cb8b6faf23b1820a39bd95d7664a27dd6143342b384e0331e51b7e7ba82b72`  
		Last Modified: Wed, 13 Mar 2024 02:26:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e2b92ebd4a717c111621c029962f2810658458c56b83348cd48ebaa4fe3068b`  
		Last Modified: Wed, 13 Mar 2024 02:26:41 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6530379ce7a04a762f33d3d224a027ad212974c8a0655010b0d6a64bc7b85c7a`  
		Last Modified: Wed, 13 Mar 2024 02:26:41 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f26449b202b587050f84dcbf4d1f5a6c2781a3ec496544a734a1c5aa6f84a47`  
		Last Modified: Wed, 13 Mar 2024 02:26:41 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b10fec8d5c8ffdc42af4071313da5e34d583a3354402e2292272981753aefd`  
		Last Modified: Wed, 13 Mar 2024 02:26:41 GMT  
		Size: 464.4 KB (464409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a24c99d6622471210ace9816e54ba35306060d852b8066456f0709d0d0a91169`  
		Last Modified: Wed, 13 Mar 2024 02:26:40 GMT  
		Size: 5.6 MB (5636561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e7f775a4d40bc0c3366839ccfff3892ca055cc7ff193756fcfebf651992727`  
		Last Modified: Wed, 13 Mar 2024 02:26:39 GMT  
		Size: 1.9 KB (1863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12930ef98a4996768cfcb1ca318dbb40c5b8fdb11e481ed1252b2bef55b83e13`  
		Last Modified: Wed, 13 Mar 2024 02:26:39 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a24b35dc5b5c0fe780138a63f9518dcebf4b9472677f95c385a5768e6139e11`  
		Last Modified: Wed, 13 Mar 2024 02:26:39 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ef9209ec4c451a237994ffe079fdb41815c69eed7e68bc677b80efd12710c2`  
		Last Modified: Wed, 13 Mar 2024 02:26:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:7a3dedb2152d01809b0343a8fce27241d6eae68f65200a8e6da78d88ac4257a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:04333a656bd283d8642c365f790bbd26a0dd2919a0d29dd75998776c6ef7207d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9577940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606a0820025fa72d87e550430e7c14c89557b69fecac16e732dbf2d3c0bcaa76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 01:47:48 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 01:47:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 01:47:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 01:47:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 01:47:51 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:47:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 01:47:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a35673fda7fb893fc2c187357a17a1c13cb7b1958fa8d97eee3155901c44fba`  
		Last Modified: Wed, 13 Mar 2024 01:48:27 GMT  
		Size: 6.2 MB (6168214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdf5efdff66ae170a3b780d793b6b5d821138b53926474870aebccb2af5ee57`  
		Last Modified: Wed, 13 Mar 2024 01:48:25 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c95813002da682382a4ba34c5210071c10314593a044ab5120d5d8780b07e4a`  
		Last Modified: Wed, 13 Mar 2024 01:48:25 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:6e93abf037354dbe3af08ece7d516f8a4e61c675fbab84594adf10b108082777
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9051274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075217343e913477fcd44713b6ae36fa6c55e5a333eca26c9e952a97e51a14f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 00:49:24 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 00:49:28 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 00:49:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 00:49:28 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 00:49:28 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:49:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 00:49:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b7bd072e2424f96ed51dee5137cd95e43686fc4624f2d2feee365fd304f5fc`  
		Last Modified: Wed, 13 Mar 2024 00:50:00 GMT  
		Size: 5.9 MB (5884880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cd491dd798da6f6a27555feb3be80ea1e29262571e10acde00300ee332740f`  
		Last Modified: Wed, 13 Mar 2024 00:49:59 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568e37ef91f5962c31828a2adc1588dcec32dbe5859699372ff1656c5659a915`  
		Last Modified: Wed, 13 Mar 2024 00:49:59 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:06913e056cdc6c1997068e0fe2e6355f571c04f12afd48f9e02cea1f16554016
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8795654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fbc0f10b6a6c92c2a77318fa3a4f9b73f5dc9a8e0304b5475f614294196d6d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 00:35:35 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 00:35:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 00:35:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 00:35:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 00:35:39 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:35:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 00:35:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55a741d01acaf5448cb8ffa39243f9f34261fd88e914772554124224189cc81`  
		Last Modified: Wed, 13 Mar 2024 00:36:23 GMT  
		Size: 5.9 MB (5875752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d61266118e4acdda142cd2ac76a4ef35e24e7502ec60b4cf26cf49a145acdc`  
		Last Modified: Wed, 13 Mar 2024 00:36:18 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1e59e375c0cd803e4186b41a2566a69e1f0a8b88ba1cf0954a5a00d33af0d2`  
		Last Modified: Wed, 13 Mar 2024 00:36:18 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:62b700c1d94d9c9164795d902681026f20a4c2c215e70dea7661f632c43f93b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9088728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b8a7d9375b33a34c6019c8a05fc253872624aaba1066208fa1ae728471c370`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 00:40:21 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 00:40:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 00:40:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 00:40:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 00:40:24 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:40:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 00:40:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46909e9837d35c1cb85abbf0a81ed8df7ac00f9ac7df67d275bd7edb87fdc88b`  
		Last Modified: Wed, 13 Mar 2024 00:41:06 GMT  
		Size: 5.7 MB (5740016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a74044cf86ca3325a7a324fbd7d08694e721bad44f2f7865d35ed3b3ce23b4`  
		Last Modified: Wed, 13 Mar 2024 00:41:05 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f776b77a6001c5e0fd42db5610aa2acfeecb867c59a3559a2cd6983a5067ad6c`  
		Last Modified: Wed, 13 Mar 2024 00:41:05 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:e73b5c826fe9e8fc554f8e4440d8ae0504b4f7899d6c5bc38c6b68a0d9e705d0
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9078995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96541c86763ab33908efa9617f909b1b23853fc66f5740829aaa97d4fb819d4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 01:28:25 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 01:28:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 01:28:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 01:28:31 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 01:28:32 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:28:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 01:28:33 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd4d0c36112be2592baa66fdba8327cff756029be8e96f803015fce9a8bfab7`  
		Last Modified: Wed, 13 Mar 2024 01:29:22 GMT  
		Size: 5.7 MB (5719643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217c8e169d797596a8b822f912ec2ba564e491f6949ecd95a5a405d275c5a5a6`  
		Last Modified: Wed, 13 Mar 2024 01:29:21 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad20a946927156b80304d831d9d123a0ba902501570002869968e92231bbd32`  
		Last Modified: Wed, 13 Mar 2024 01:29:21 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:49f1c4fa564a8f8073315103db29d373273c7e703c43d6f275a1acc3ab010a3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9296162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7420d0049b07e2c363f050c33e0ac3ba0fe39fe6d0bee0ffea5c71f2fdf0749`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 01:14:00 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 01:14:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 01:14:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 01:14:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 01:14:03 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:14:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 01:14:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d4a8da7be6313cc596f154b85b638749ab970144f58575af5bef288a9e44ce`  
		Last Modified: Wed, 13 Mar 2024 01:16:34 GMT  
		Size: 6.1 MB (6052529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c87220ce1b5f8a7ed2e5ab6caf39ac9028ba6d25133711633f25a21b60c4b24`  
		Last Modified: Wed, 13 Mar 2024 01:16:33 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43f30dc994a90cc1c2a38e8a5176d279817dd3d25ffe3d8ac67b665c606f3b3`  
		Last Modified: Wed, 13 Mar 2024 01:16:33 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.19`

```console
$ docker pull nats@sha256:7a3dedb2152d01809b0343a8fce27241d6eae68f65200a8e6da78d88ac4257a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:alpine3.19` - linux; amd64

```console
$ docker pull nats@sha256:04333a656bd283d8642c365f790bbd26a0dd2919a0d29dd75998776c6ef7207d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9577940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606a0820025fa72d87e550430e7c14c89557b69fecac16e732dbf2d3c0bcaa76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 01:47:48 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 01:47:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 01:47:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 01:47:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 01:47:51 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:47:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 01:47:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a35673fda7fb893fc2c187357a17a1c13cb7b1958fa8d97eee3155901c44fba`  
		Last Modified: Wed, 13 Mar 2024 01:48:27 GMT  
		Size: 6.2 MB (6168214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdf5efdff66ae170a3b780d793b6b5d821138b53926474870aebccb2af5ee57`  
		Last Modified: Wed, 13 Mar 2024 01:48:25 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c95813002da682382a4ba34c5210071c10314593a044ab5120d5d8780b07e4a`  
		Last Modified: Wed, 13 Mar 2024 01:48:25 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; arm variant v6

```console
$ docker pull nats@sha256:6e93abf037354dbe3af08ece7d516f8a4e61c675fbab84594adf10b108082777
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9051274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075217343e913477fcd44713b6ae36fa6c55e5a333eca26c9e952a97e51a14f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 00:49:24 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 00:49:28 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 00:49:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 00:49:28 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 00:49:28 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:49:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 00:49:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b7bd072e2424f96ed51dee5137cd95e43686fc4624f2d2feee365fd304f5fc`  
		Last Modified: Wed, 13 Mar 2024 00:50:00 GMT  
		Size: 5.9 MB (5884880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cd491dd798da6f6a27555feb3be80ea1e29262571e10acde00300ee332740f`  
		Last Modified: Wed, 13 Mar 2024 00:49:59 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568e37ef91f5962c31828a2adc1588dcec32dbe5859699372ff1656c5659a915`  
		Last Modified: Wed, 13 Mar 2024 00:49:59 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:06913e056cdc6c1997068e0fe2e6355f571c04f12afd48f9e02cea1f16554016
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8795654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fbc0f10b6a6c92c2a77318fa3a4f9b73f5dc9a8e0304b5475f614294196d6d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 00:35:35 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 00:35:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 00:35:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 00:35:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 00:35:39 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:35:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 00:35:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55a741d01acaf5448cb8ffa39243f9f34261fd88e914772554124224189cc81`  
		Last Modified: Wed, 13 Mar 2024 00:36:23 GMT  
		Size: 5.9 MB (5875752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d61266118e4acdda142cd2ac76a4ef35e24e7502ec60b4cf26cf49a145acdc`  
		Last Modified: Wed, 13 Mar 2024 00:36:18 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1e59e375c0cd803e4186b41a2566a69e1f0a8b88ba1cf0954a5a00d33af0d2`  
		Last Modified: Wed, 13 Mar 2024 00:36:18 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:62b700c1d94d9c9164795d902681026f20a4c2c215e70dea7661f632c43f93b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9088728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b8a7d9375b33a34c6019c8a05fc253872624aaba1066208fa1ae728471c370`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 00:40:21 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 00:40:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 00:40:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 00:40:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 00:40:24 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:40:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 00:40:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46909e9837d35c1cb85abbf0a81ed8df7ac00f9ac7df67d275bd7edb87fdc88b`  
		Last Modified: Wed, 13 Mar 2024 00:41:06 GMT  
		Size: 5.7 MB (5740016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a74044cf86ca3325a7a324fbd7d08694e721bad44f2f7865d35ed3b3ce23b4`  
		Last Modified: Wed, 13 Mar 2024 00:41:05 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f776b77a6001c5e0fd42db5610aa2acfeecb867c59a3559a2cd6983a5067ad6c`  
		Last Modified: Wed, 13 Mar 2024 00:41:05 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; ppc64le

```console
$ docker pull nats@sha256:e73b5c826fe9e8fc554f8e4440d8ae0504b4f7899d6c5bc38c6b68a0d9e705d0
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9078995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96541c86763ab33908efa9617f909b1b23853fc66f5740829aaa97d4fb819d4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 01:28:25 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 01:28:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 01:28:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 01:28:31 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 01:28:32 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:28:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 01:28:33 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd4d0c36112be2592baa66fdba8327cff756029be8e96f803015fce9a8bfab7`  
		Last Modified: Wed, 13 Mar 2024 01:29:22 GMT  
		Size: 5.7 MB (5719643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217c8e169d797596a8b822f912ec2ba564e491f6949ecd95a5a405d275c5a5a6`  
		Last Modified: Wed, 13 Mar 2024 01:29:21 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad20a946927156b80304d831d9d123a0ba902501570002869968e92231bbd32`  
		Last Modified: Wed, 13 Mar 2024 01:29:21 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; s390x

```console
$ docker pull nats@sha256:49f1c4fa564a8f8073315103db29d373273c7e703c43d6f275a1acc3ab010a3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9296162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7420d0049b07e2c363f050c33e0ac3ba0fe39fe6d0bee0ffea5c71f2fdf0749`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 01:14:00 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 01:14:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 01:14:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 01:14:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 01:14:03 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:14:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 01:14:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d4a8da7be6313cc596f154b85b638749ab970144f58575af5bef288a9e44ce`  
		Last Modified: Wed, 13 Mar 2024 01:16:34 GMT  
		Size: 6.1 MB (6052529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c87220ce1b5f8a7ed2e5ab6caf39ac9028ba6d25133711633f25a21b60c4b24`  
		Last Modified: Wed, 13 Mar 2024 01:16:33 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43f30dc994a90cc1c2a38e8a5176d279817dd3d25ffe3d8ac67b665c606f3b3`  
		Last Modified: Wed, 13 Mar 2024 01:16:33 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:9b1ee0caf5737f6b44b15da670b866900af4077d6ae6e2a170466e2e0fc68cb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5576; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:6fb1a85021a8411e0470cca8a43d461db915d2df605657389c4f0595d2e42e91
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5548142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8780d448219e4996eb219326ba6943b7e05f04ab1189a6f1dcf2e013058e3e36`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:47:57 GMT
COPY file:33d3e4ce6e17dc907ca0b478996354d26d433431b7bf48ae5bef3ec2ea1359f1 in /nats-server 
# Wed, 13 Mar 2024 01:47:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:47:57 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:47:57 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:47:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce8539fabe7af34129953a073c64515d008d19eac52a820ef52368f6411e540d`  
		Last Modified: Wed, 13 Mar 2024 01:48:46 GMT  
		Size: 5.5 MB (5547633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5208dae10516783bd9b5be071d7f3d39c84e1138b3887856c85f570ec4f588c`  
		Last Modified: Wed, 13 Mar 2024 01:48:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:b717fb731a88e81bdabf9b7eb28e2ee0fa423ff801dcd5819fb4ffaf217cb208
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5263761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51552a7d22c2c5ca2447ff2b4198de16cfdff9a116a3c54ef5af0d997a9469f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:49:35 GMT
COPY file:c24c6855bab6e8b64a222738f44249dd58afe5ec56a34cfd64493e736f5325df in /nats-server 
# Wed, 13 Mar 2024 00:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:49:35 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:49:35 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:49:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bc2b5fa4421ea8f446fd52c0a8e7c8c6e048dc4aa6a096fb60765aa281147267`  
		Last Modified: Wed, 13 Mar 2024 00:50:20 GMT  
		Size: 5.3 MB (5263253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652cf78472b592b1ea355485d1a353340ba41c0d01b26f15ffacc090db84d7bb`  
		Last Modified: Wed, 13 Mar 2024 00:50:19 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:07d02d1f567ff67a36ece1f90364e466f099db860d2e8ec1f2143bec1c3710f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5956a4e3835d4532ea5cbfc23f7b2e2d96d15a877f42392feea63afa16be107b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:35:52 GMT
COPY file:6899efa16d7091375dc53de2fc1e5686e82569d9799d6cede2e40b0a8b6abb48 in /nats-server 
# Wed, 13 Mar 2024 00:35:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:35:52 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:35:52 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:35:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:68296288971fdb3ddfe9bfba9b6a79725a69e891fb82cd5708f088afaac9929f`  
		Last Modified: Wed, 13 Mar 2024 00:36:43 GMT  
		Size: 5.3 MB (5254529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652026202bce83174144280de06b0537518e9d13e1674ac88f0d7e8491a2e440`  
		Last Modified: Wed, 13 Mar 2024 00:36:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f8017338e2c0dd9d3adb17672dd8226d475d5c810fa5f742c27a1d77f6e0c0e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8216507954fc8ffbaa79f3aa0908756fb3b5e699a13215671cf23837d30ca343`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:40:40 GMT
COPY file:674069719b01a345db55aa1ea35485a8b6f0cf0eed465ae05a0c00073e2ab2ab in /nats-server 
# Wed, 13 Mar 2024 00:40:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:40:40 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:40:40 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:40:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d5466aeaf1139b432e415e6412234c167a91220e74d17f50be1a2de5b0fb1b21`  
		Last Modified: Wed, 13 Mar 2024 00:41:26 GMT  
		Size: 5.1 MB (5117178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562c0bd40d1b70ec911e4b7219f7867675e2ad1c67899a3643f13d261d792187`  
		Last Modified: Wed, 13 Mar 2024 00:41:25 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:e964ace9a5047268966aa2f1f2e10472325f21ac790016722c0a9090997a39f1
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a273f9d6d6aa560ff8df97aee7e4c13f87044f2be0081b07ba0f4a0fafd81a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 16 Feb 2024 19:24:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:29:00 GMT
COPY file:0e1c98477f605478a27423b67d1c7bf88d4b2a56d0696ea31430a8a59b294dd8 in /nats-server 
# Wed, 13 Mar 2024 01:29:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:29:01 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:29:01 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:29:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7eaf17599ba122502fe00d1cb4014722df0b46a83f614f9430f71b816a6999f8`  
		Last Modified: Wed, 13 Mar 2024 01:29:44 GMT  
		Size: 5.1 MB (5096748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b8d7d148d9f2f60c0b13204daf3a2f76ff85991d79fe4fd82aa842a3d77a1d`  
		Last Modified: Wed, 13 Mar 2024 01:29:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:21d23f9777f88070c60ce8bf669dd9169ad10d91ddae1f43c02b5419cc5fcbc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5430830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a9daecac5ba461be180b94ca61fe053ebe1e5c23af8e61522f1854982e6157`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:15:09 GMT
COPY file:cc94c349de0e266f428d63773845fb669334304c5fbcffeec57553d333126f22 in /nats-server 
# Wed, 13 Mar 2024 01:15:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:15:09 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:15:09 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:15:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0bf838b872f1e012c580bbff8d1e66a09a7b05a85651db222851ea3323dab3d2`  
		Last Modified: Wed, 13 Mar 2024 01:16:47 GMT  
		Size: 5.4 MB (5430321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668de88817078f4ef2cf284dff428f40567f94b7132efee56fe3abe6264e6d42`  
		Last Modified: Wed, 13 Mar 2024 01:16:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats@sha256:1bb4572909b97a5aea3e76230e9d09a1078a21d41ba7000bd5afbe5225fc1568
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110290182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a1f3d16c6f5aea885d55ec76e40c984ca8763448ae4b9b424ec4d5bec24fc8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 02:21:55 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:21:57 GMT
RUN cmd /S /C #(nop) COPY file:b8b09037eca4c9daccbaf940396fb084777535cdce4ec562f44c0b727cf16e3e in C:\nats-server.exe 
# Wed, 13 Mar 2024 02:21:57 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Mar 2024 02:21:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 02:21:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Mar 2024 02:21:59 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e772fbc90f54f9eab2951a9615b88e9eca8fc78909aba2cb3678cc214eb88ae2`  
		Last Modified: Wed, 13 Mar 2024 02:26:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9cd82df1e1baf71960c98c3ca3996de090e25ce522c16d07628ea7705a1c7b`  
		Last Modified: Wed, 13 Mar 2024 02:26:26 GMT  
		Size: 5.7 MB (5663658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce47417df81557c57ff79790516751ae140155b5d06e2f8538fcf4d7e94a1004`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c07d5748899da1f68ed98e7331fa02c4175552921ad31f2ec6ba40f208c69d`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89220da9dce87f2d7ea149e170563fa7bac7ae732a1b8c89f51d60e5da18020e`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78635ce16de8337563a88c3a78835fed97c207dc9254d2dc0d06594b9926b0e0`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:bb90d21b87ba223e838d39e5ee66ebeea8b63e8a6bffb4a2b19f5b291e46d1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:6fb1a85021a8411e0470cca8a43d461db915d2df605657389c4f0595d2e42e91
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5548142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8780d448219e4996eb219326ba6943b7e05f04ab1189a6f1dcf2e013058e3e36`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:47:57 GMT
COPY file:33d3e4ce6e17dc907ca0b478996354d26d433431b7bf48ae5bef3ec2ea1359f1 in /nats-server 
# Wed, 13 Mar 2024 01:47:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:47:57 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:47:57 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:47:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce8539fabe7af34129953a073c64515d008d19eac52a820ef52368f6411e540d`  
		Last Modified: Wed, 13 Mar 2024 01:48:46 GMT  
		Size: 5.5 MB (5547633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5208dae10516783bd9b5be071d7f3d39c84e1138b3887856c85f570ec4f588c`  
		Last Modified: Wed, 13 Mar 2024 01:48:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:b717fb731a88e81bdabf9b7eb28e2ee0fa423ff801dcd5819fb4ffaf217cb208
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5263761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51552a7d22c2c5ca2447ff2b4198de16cfdff9a116a3c54ef5af0d997a9469f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:49:35 GMT
COPY file:c24c6855bab6e8b64a222738f44249dd58afe5ec56a34cfd64493e736f5325df in /nats-server 
# Wed, 13 Mar 2024 00:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:49:35 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:49:35 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:49:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bc2b5fa4421ea8f446fd52c0a8e7c8c6e048dc4aa6a096fb60765aa281147267`  
		Last Modified: Wed, 13 Mar 2024 00:50:20 GMT  
		Size: 5.3 MB (5263253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652cf78472b592b1ea355485d1a353340ba41c0d01b26f15ffacc090db84d7bb`  
		Last Modified: Wed, 13 Mar 2024 00:50:19 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:07d02d1f567ff67a36ece1f90364e466f099db860d2e8ec1f2143bec1c3710f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5956a4e3835d4532ea5cbfc23f7b2e2d96d15a877f42392feea63afa16be107b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:35:52 GMT
COPY file:6899efa16d7091375dc53de2fc1e5686e82569d9799d6cede2e40b0a8b6abb48 in /nats-server 
# Wed, 13 Mar 2024 00:35:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:35:52 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:35:52 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:35:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:68296288971fdb3ddfe9bfba9b6a79725a69e891fb82cd5708f088afaac9929f`  
		Last Modified: Wed, 13 Mar 2024 00:36:43 GMT  
		Size: 5.3 MB (5254529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652026202bce83174144280de06b0537518e9d13e1674ac88f0d7e8491a2e440`  
		Last Modified: Wed, 13 Mar 2024 00:36:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f8017338e2c0dd9d3adb17672dd8226d475d5c810fa5f742c27a1d77f6e0c0e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8216507954fc8ffbaa79f3aa0908756fb3b5e699a13215671cf23837d30ca343`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:40:40 GMT
COPY file:674069719b01a345db55aa1ea35485a8b6f0cf0eed465ae05a0c00073e2ab2ab in /nats-server 
# Wed, 13 Mar 2024 00:40:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:40:40 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:40:40 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:40:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d5466aeaf1139b432e415e6412234c167a91220e74d17f50be1a2de5b0fb1b21`  
		Last Modified: Wed, 13 Mar 2024 00:41:26 GMT  
		Size: 5.1 MB (5117178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562c0bd40d1b70ec911e4b7219f7867675e2ad1c67899a3643f13d261d792187`  
		Last Modified: Wed, 13 Mar 2024 00:41:25 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:e964ace9a5047268966aa2f1f2e10472325f21ac790016722c0a9090997a39f1
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a273f9d6d6aa560ff8df97aee7e4c13f87044f2be0081b07ba0f4a0fafd81a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 16 Feb 2024 19:24:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:29:00 GMT
COPY file:0e1c98477f605478a27423b67d1c7bf88d4b2a56d0696ea31430a8a59b294dd8 in /nats-server 
# Wed, 13 Mar 2024 01:29:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:29:01 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:29:01 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:29:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7eaf17599ba122502fe00d1cb4014722df0b46a83f614f9430f71b816a6999f8`  
		Last Modified: Wed, 13 Mar 2024 01:29:44 GMT  
		Size: 5.1 MB (5096748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b8d7d148d9f2f60c0b13204daf3a2f76ff85991d79fe4fd82aa842a3d77a1d`  
		Last Modified: Wed, 13 Mar 2024 01:29:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:21d23f9777f88070c60ce8bf669dd9169ad10d91ddae1f43c02b5419cc5fcbc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5430830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a9daecac5ba461be180b94ca61fe053ebe1e5c23af8e61522f1854982e6157`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:15:09 GMT
COPY file:cc94c349de0e266f428d63773845fb669334304c5fbcffeec57553d333126f22 in /nats-server 
# Wed, 13 Mar 2024 01:15:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:15:09 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:15:09 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:15:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0bf838b872f1e012c580bbff8d1e66a09a7b05a85651db222851ea3323dab3d2`  
		Last Modified: Wed, 13 Mar 2024 01:16:47 GMT  
		Size: 5.4 MB (5430321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668de88817078f4ef2cf284dff428f40567f94b7132efee56fe3abe6264e6d42`  
		Last Modified: Wed, 13 Mar 2024 01:16:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:38b381e6f2834d3c5120087f02c9d13f238a2142f54568a208fa74d554bb62d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats:nanoserver` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats@sha256:1bb4572909b97a5aea3e76230e9d09a1078a21d41ba7000bd5afbe5225fc1568
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110290182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a1f3d16c6f5aea885d55ec76e40c984ca8763448ae4b9b424ec4d5bec24fc8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 02:21:55 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:21:57 GMT
RUN cmd /S /C #(nop) COPY file:b8b09037eca4c9daccbaf940396fb084777535cdce4ec562f44c0b727cf16e3e in C:\nats-server.exe 
# Wed, 13 Mar 2024 02:21:57 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Mar 2024 02:21:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 02:21:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Mar 2024 02:21:59 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e772fbc90f54f9eab2951a9615b88e9eca8fc78909aba2cb3678cc214eb88ae2`  
		Last Modified: Wed, 13 Mar 2024 02:26:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9cd82df1e1baf71960c98c3ca3996de090e25ce522c16d07628ea7705a1c7b`  
		Last Modified: Wed, 13 Mar 2024 02:26:26 GMT  
		Size: 5.7 MB (5663658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce47417df81557c57ff79790516751ae140155b5d06e2f8538fcf4d7e94a1004`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c07d5748899da1f68ed98e7331fa02c4175552921ad31f2ec6ba40f208c69d`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89220da9dce87f2d7ea149e170563fa7bac7ae732a1b8c89f51d60e5da18020e`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78635ce16de8337563a88c3a78835fed97c207dc9254d2dc0d06594b9926b0e0`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:38b381e6f2834d3c5120087f02c9d13f238a2142f54568a208fa74d554bb62d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats@sha256:1bb4572909b97a5aea3e76230e9d09a1078a21d41ba7000bd5afbe5225fc1568
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110290182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a1f3d16c6f5aea885d55ec76e40c984ca8763448ae4b9b424ec4d5bec24fc8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 02:21:55 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:21:57 GMT
RUN cmd /S /C #(nop) COPY file:b8b09037eca4c9daccbaf940396fb084777535cdce4ec562f44c0b727cf16e3e in C:\nats-server.exe 
# Wed, 13 Mar 2024 02:21:57 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Mar 2024 02:21:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 02:21:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Mar 2024 02:21:59 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e772fbc90f54f9eab2951a9615b88e9eca8fc78909aba2cb3678cc214eb88ae2`  
		Last Modified: Wed, 13 Mar 2024 02:26:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9cd82df1e1baf71960c98c3ca3996de090e25ce522c16d07628ea7705a1c7b`  
		Last Modified: Wed, 13 Mar 2024 02:26:26 GMT  
		Size: 5.7 MB (5663658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce47417df81557c57ff79790516751ae140155b5d06e2f8538fcf4d7e94a1004`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c07d5748899da1f68ed98e7331fa02c4175552921ad31f2ec6ba40f208c69d`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89220da9dce87f2d7ea149e170563fa7bac7ae732a1b8c89f51d60e5da18020e`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78635ce16de8337563a88c3a78835fed97c207dc9254d2dc0d06594b9926b0e0`  
		Last Modified: Wed, 13 Mar 2024 02:26:25 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:bb90d21b87ba223e838d39e5ee66ebeea8b63e8a6bffb4a2b19f5b291e46d1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:6fb1a85021a8411e0470cca8a43d461db915d2df605657389c4f0595d2e42e91
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5548142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8780d448219e4996eb219326ba6943b7e05f04ab1189a6f1dcf2e013058e3e36`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:47:57 GMT
COPY file:33d3e4ce6e17dc907ca0b478996354d26d433431b7bf48ae5bef3ec2ea1359f1 in /nats-server 
# Wed, 13 Mar 2024 01:47:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:47:57 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:47:57 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:47:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce8539fabe7af34129953a073c64515d008d19eac52a820ef52368f6411e540d`  
		Last Modified: Wed, 13 Mar 2024 01:48:46 GMT  
		Size: 5.5 MB (5547633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5208dae10516783bd9b5be071d7f3d39c84e1138b3887856c85f570ec4f588c`  
		Last Modified: Wed, 13 Mar 2024 01:48:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:b717fb731a88e81bdabf9b7eb28e2ee0fa423ff801dcd5819fb4ffaf217cb208
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5263761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51552a7d22c2c5ca2447ff2b4198de16cfdff9a116a3c54ef5af0d997a9469f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:49:35 GMT
COPY file:c24c6855bab6e8b64a222738f44249dd58afe5ec56a34cfd64493e736f5325df in /nats-server 
# Wed, 13 Mar 2024 00:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:49:35 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:49:35 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:49:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bc2b5fa4421ea8f446fd52c0a8e7c8c6e048dc4aa6a096fb60765aa281147267`  
		Last Modified: Wed, 13 Mar 2024 00:50:20 GMT  
		Size: 5.3 MB (5263253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652cf78472b592b1ea355485d1a353340ba41c0d01b26f15ffacc090db84d7bb`  
		Last Modified: Wed, 13 Mar 2024 00:50:19 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:07d02d1f567ff67a36ece1f90364e466f099db860d2e8ec1f2143bec1c3710f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5956a4e3835d4532ea5cbfc23f7b2e2d96d15a877f42392feea63afa16be107b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:35:52 GMT
COPY file:6899efa16d7091375dc53de2fc1e5686e82569d9799d6cede2e40b0a8b6abb48 in /nats-server 
# Wed, 13 Mar 2024 00:35:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:35:52 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:35:52 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:35:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:68296288971fdb3ddfe9bfba9b6a79725a69e891fb82cd5708f088afaac9929f`  
		Last Modified: Wed, 13 Mar 2024 00:36:43 GMT  
		Size: 5.3 MB (5254529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652026202bce83174144280de06b0537518e9d13e1674ac88f0d7e8491a2e440`  
		Last Modified: Wed, 13 Mar 2024 00:36:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f8017338e2c0dd9d3adb17672dd8226d475d5c810fa5f742c27a1d77f6e0c0e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8216507954fc8ffbaa79f3aa0908756fb3b5e699a13215671cf23837d30ca343`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:40:40 GMT
COPY file:674069719b01a345db55aa1ea35485a8b6f0cf0eed465ae05a0c00073e2ab2ab in /nats-server 
# Wed, 13 Mar 2024 00:40:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:40:40 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:40:40 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:40:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d5466aeaf1139b432e415e6412234c167a91220e74d17f50be1a2de5b0fb1b21`  
		Last Modified: Wed, 13 Mar 2024 00:41:26 GMT  
		Size: 5.1 MB (5117178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562c0bd40d1b70ec911e4b7219f7867675e2ad1c67899a3643f13d261d792187`  
		Last Modified: Wed, 13 Mar 2024 00:41:25 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:e964ace9a5047268966aa2f1f2e10472325f21ac790016722c0a9090997a39f1
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a273f9d6d6aa560ff8df97aee7e4c13f87044f2be0081b07ba0f4a0fafd81a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 16 Feb 2024 19:24:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:29:00 GMT
COPY file:0e1c98477f605478a27423b67d1c7bf88d4b2a56d0696ea31430a8a59b294dd8 in /nats-server 
# Wed, 13 Mar 2024 01:29:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:29:01 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:29:01 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:29:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7eaf17599ba122502fe00d1cb4014722df0b46a83f614f9430f71b816a6999f8`  
		Last Modified: Wed, 13 Mar 2024 01:29:44 GMT  
		Size: 5.1 MB (5096748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b8d7d148d9f2f60c0b13204daf3a2f76ff85991d79fe4fd82aa842a3d77a1d`  
		Last Modified: Wed, 13 Mar 2024 01:29:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:21d23f9777f88070c60ce8bf669dd9169ad10d91ddae1f43c02b5419cc5fcbc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5430830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a9daecac5ba461be180b94ca61fe053ebe1e5c23af8e61522f1854982e6157`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:15:09 GMT
COPY file:cc94c349de0e266f428d63773845fb669334304c5fbcffeec57553d333126f22 in /nats-server 
# Wed, 13 Mar 2024 01:15:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:15:09 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:15:09 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:15:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0bf838b872f1e012c580bbff8d1e66a09a7b05a85651db222851ea3323dab3d2`  
		Last Modified: Wed, 13 Mar 2024 01:16:47 GMT  
		Size: 5.4 MB (5430321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668de88817078f4ef2cf284dff428f40567f94b7132efee56fe3abe6264e6d42`  
		Last Modified: Wed, 13 Mar 2024 01:16:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:d7d19aca6454b871d5135f9cc685694349f0f72c02f00641f749e391f828e8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats:windowsservercore` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats@sha256:7fa1366a0cee4e50f2a2402c01dd3ea274be364140f556693350356d0e2db63c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2131507333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3743311440c84bac2fc9c9e5e74770053c07f4480d2901f7abe6813c87cf4dae`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 02:18:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Mar 2024 02:18:28 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:18:29 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 02:18:30 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.12/nats-server-v2.10.12-windows-amd64.zip
# Wed, 13 Mar 2024 02:18:30 GMT
ENV NATS_SERVER_SHASUM=bc944f832fdc3eaa0072c0a5e278efd672cec394159661070e7aea4f5d483cbc
# Wed, 13 Mar 2024 02:19:47 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Mar 2024 02:21:44 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 13 Mar 2024 02:21:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Mar 2024 02:21:45 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 02:21:46 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Mar 2024 02:21:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e169e85f3c664d99b16235c550eb744e7e1421ceb3b4a239fd727321ccddc77`  
		Last Modified: Wed, 13 Mar 2024 02:26:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7cb8b6faf23b1820a39bd95d7664a27dd6143342b384e0331e51b7e7ba82b72`  
		Last Modified: Wed, 13 Mar 2024 02:26:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3886c92295e481a562d7a5fe9418c1de632210a05c19f06705629bc95800902`  
		Last Modified: Wed, 13 Mar 2024 02:26:10 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b851f5dbeec69a3c0b7cef01f0be439c3febe18363296e9980de2f7ba04d04ec`  
		Last Modified: Wed, 13 Mar 2024 02:26:10 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ac0c5c4d4063f650788f99bee2df77584d4cce33709529fbf1c1287c77e6b1`  
		Last Modified: Wed, 13 Mar 2024 02:26:10 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce303014e2084243978d691011a901e05e79a3dd3aca02f6bf15b0111f313ba`  
		Last Modified: Wed, 13 Mar 2024 02:26:10 GMT  
		Size: 445.8 KB (445828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209561aab82234ce8e269b77a1c45eb4d10f5c3d9ec877e078db4d5b72ab672c`  
		Last Modified: Wed, 13 Mar 2024 02:26:09 GMT  
		Size: 5.9 MB (5948270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b859631a59ecabb2bf06bbe8d86a2994232ad2d5852842b40363bf2bbb528cc7`  
		Last Modified: Wed, 13 Mar 2024 02:26:08 GMT  
		Size: 2.0 KB (1985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b5005070ee0dabaf577a0f2e898332aab7a1ec26da577b3d2ceb9ffeaaf343`  
		Last Modified: Wed, 13 Mar 2024 02:26:08 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4db2f7ed46b07e7feccb03f8e63ad91142de5165acf6c898a5aac89b0cd559`  
		Last Modified: Wed, 13 Mar 2024 02:26:08 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81813a03072d63cfbad1f640180a29dfc80c337f2a4ffeaeb116769574cda27`  
		Last Modified: Wed, 13 Mar 2024 02:26:08 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:d7d19aca6454b871d5135f9cc685694349f0f72c02f00641f749e391f828e8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats@sha256:7fa1366a0cee4e50f2a2402c01dd3ea274be364140f556693350356d0e2db63c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2131507333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3743311440c84bac2fc9c9e5e74770053c07f4480d2901f7abe6813c87cf4dae`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 02:18:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Mar 2024 02:18:28 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:18:29 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 02:18:30 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.12/nats-server-v2.10.12-windows-amd64.zip
# Wed, 13 Mar 2024 02:18:30 GMT
ENV NATS_SERVER_SHASUM=bc944f832fdc3eaa0072c0a5e278efd672cec394159661070e7aea4f5d483cbc
# Wed, 13 Mar 2024 02:19:47 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Mar 2024 02:21:44 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 13 Mar 2024 02:21:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Mar 2024 02:21:45 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 02:21:46 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Mar 2024 02:21:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e169e85f3c664d99b16235c550eb744e7e1421ceb3b4a239fd727321ccddc77`  
		Last Modified: Wed, 13 Mar 2024 02:26:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7cb8b6faf23b1820a39bd95d7664a27dd6143342b384e0331e51b7e7ba82b72`  
		Last Modified: Wed, 13 Mar 2024 02:26:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3886c92295e481a562d7a5fe9418c1de632210a05c19f06705629bc95800902`  
		Last Modified: Wed, 13 Mar 2024 02:26:10 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b851f5dbeec69a3c0b7cef01f0be439c3febe18363296e9980de2f7ba04d04ec`  
		Last Modified: Wed, 13 Mar 2024 02:26:10 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ac0c5c4d4063f650788f99bee2df77584d4cce33709529fbf1c1287c77e6b1`  
		Last Modified: Wed, 13 Mar 2024 02:26:10 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce303014e2084243978d691011a901e05e79a3dd3aca02f6bf15b0111f313ba`  
		Last Modified: Wed, 13 Mar 2024 02:26:10 GMT  
		Size: 445.8 KB (445828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209561aab82234ce8e269b77a1c45eb4d10f5c3d9ec877e078db4d5b72ab672c`  
		Last Modified: Wed, 13 Mar 2024 02:26:09 GMT  
		Size: 5.9 MB (5948270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b859631a59ecabb2bf06bbe8d86a2994232ad2d5852842b40363bf2bbb528cc7`  
		Last Modified: Wed, 13 Mar 2024 02:26:08 GMT  
		Size: 2.0 KB (1985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b5005070ee0dabaf577a0f2e898332aab7a1ec26da577b3d2ceb9ffeaaf343`  
		Last Modified: Wed, 13 Mar 2024 02:26:08 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4db2f7ed46b07e7feccb03f8e63ad91142de5165acf6c898a5aac89b0cd559`  
		Last Modified: Wed, 13 Mar 2024 02:26:08 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81813a03072d63cfbad1f640180a29dfc80c337f2a4ffeaeb116769574cda27`  
		Last Modified: Wed, 13 Mar 2024 02:26:08 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
