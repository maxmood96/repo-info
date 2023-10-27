<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.18`](#nats2-alpine318)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2.10`](#nats210)
-	[`nats:2.10-alpine`](#nats210-alpine)
-	[`nats:2.10-alpine3.18`](#nats210-alpine318)
-	[`nats:2.10-linux`](#nats210-linux)
-	[`nats:2.10-nanoserver`](#nats210-nanoserver)
-	[`nats:2.10-nanoserver-1809`](#nats210-nanoserver-1809)
-	[`nats:2.10-scratch`](#nats210-scratch)
-	[`nats:2.10-windowsservercore`](#nats210-windowsservercore)
-	[`nats:2.10-windowsservercore-1809`](#nats210-windowsservercore-1809)
-	[`nats:2.10.4`](#nats2104)
-	[`nats:2.10.4-alpine`](#nats2104-alpine)
-	[`nats:2.10.4-alpine3.18`](#nats2104-alpine318)
-	[`nats:2.10.4-linux`](#nats2104-linux)
-	[`nats:2.10.4-nanoserver`](#nats2104-nanoserver)
-	[`nats:2.10.4-nanoserver-1809`](#nats2104-nanoserver-1809)
-	[`nats:2.10.4-scratch`](#nats2104-scratch)
-	[`nats:2.10.4-windowsservercore`](#nats2104-windowsservercore)
-	[`nats:2.10.4-windowsservercore-1809`](#nats2104-windowsservercore-1809)
-	[`nats:2.9`](#nats29)
-	[`nats:2.9-alpine`](#nats29-alpine)
-	[`nats:2.9-alpine3.18`](#nats29-alpine318)
-	[`nats:2.9-linux`](#nats29-linux)
-	[`nats:2.9-nanoserver`](#nats29-nanoserver)
-	[`nats:2.9-nanoserver-1809`](#nats29-nanoserver-1809)
-	[`nats:2.9-scratch`](#nats29-scratch)
-	[`nats:2.9-windowsservercore`](#nats29-windowsservercore)
-	[`nats:2.9-windowsservercore-1809`](#nats29-windowsservercore-1809)
-	[`nats:2.9.23`](#nats2923)
-	[`nats:2.9.23-alpine`](#nats2923-alpine)
-	[`nats:2.9.23-alpine3.18`](#nats2923-alpine318)
-	[`nats:2.9.23-linux`](#nats2923-linux)
-	[`nats:2.9.23-nanoserver`](#nats2923-nanoserver)
-	[`nats:2.9.23-nanoserver-1809`](#nats2923-nanoserver-1809)
-	[`nats:2.9.23-scratch`](#nats2923-scratch)
-	[`nats:2.9.23-windowsservercore`](#nats2923-windowsservercore)
-	[`nats:2.9.23-windowsservercore-1809`](#nats2923-windowsservercore-1809)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.18`](#natsalpine318)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)

## `nats:2`

```console
$ docker pull nats@sha256:ab462f647d9460c169dde8a382ec59675ed1f65bad4617dbc9f1f007bd5a709b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4974; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:fe0f6382b8b6b1820004268a1e539cabf394046302ddb9bd1fe14be1d5771fbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5481847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211d523019caad51116b188eb0cf75ce76becdb5aa40535a9f786d29130792f4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:24:45 GMT
COPY file:8488714a53ceca0afd69fdc135a2e59f81f3008e24d351a22438b39d8ab405fe in /nats-server 
# Fri, 27 Oct 2023 19:24:45 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:24:45 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:24:45 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:24:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:db9df0ffe6fe1654cbad22b0ee4be8b11d47faa0ee2c6f353915285f56329500`  
		Last Modified: Fri, 27 Oct 2023 19:25:41 GMT  
		Size: 5.5 MB (5481338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89fadd4ca8047bf736c814f88e92efa539731e382b4419dee4eee68edbe42fe`  
		Last Modified: Fri, 27 Oct 2023 19:25:40 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:7d149a46fee148c37fa3b2bca97ac72ab1f96ed1793f8114cfecb40adc754119
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5247112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d7fa3037dc87b27de3f83d3dcb521067502705385f652d472d31fa037af822`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 02:39:39 GMT
COPY file:71487567f54b75938083a2680d411bd9e194b037c12b743a3c280c58abd7e82f in /nats-server 
# Sat, 21 Oct 2023 02:39:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 02:39:39 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 02:39:40 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 02:39:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5d153758a0dd20c137d358179ec27f8aca298056d0b26005f90208c882f0c7fa`  
		Last Modified: Fri, 13 Oct 2023 20:22:03 GMT  
		Size: 5.2 MB (5246604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e10c8d3bbc8928c41b93c6acf289f4b157e058ca08c00bee7222d13f60ce5b`  
		Last Modified: Sat, 21 Oct 2023 02:40:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:b86c68503d84530fc3cb5ab2b6020dfe898e9e6d9b56965c14886b3cbdb07fd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5200382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7fef18696d3fe7987d9a9cbb167d045bcf97d5d2a1ac6fb76e73c65abde696`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:49:36 GMT
COPY file:0b4bcbfc47b21cd20c0f98a685ba4fbd4a6e7c8df6268e72fa48d2886a177781 in /nats-server 
# Fri, 27 Oct 2023 19:49:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:49:36 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:260eff5507dab2d5105a6c9ea84fc78fb51e66c5435f05572b8f8e7767cb103d`  
		Last Modified: Fri, 27 Oct 2023 19:50:29 GMT  
		Size: 5.2 MB (5199874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2e9e51baf6f1fddbeae98b8fed44bf52c3b147232cdea2f33fe5943fa9dc31`  
		Last Modified: Fri, 27 Oct 2023 19:50:28 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:e80d5b10ed40caa3cae83ffa38af5ef4bb0c64e0a2174439dac89888d070cfc3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4983318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f65e0f853a25dd0c5e95c7b124ee834aafd668a27728562f5992e6bf60bce3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 00:29:27 GMT
COPY file:a99ff6735b1292770195e5dfe0e7f8a56bae939bfb272c8cbdfb47e7ba6c4828 in /nats-server 
# Sat, 21 Oct 2023 00:29:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 00:29:27 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 00:29:27 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 00:29:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:217c24d6cc08c267f56e5da2ce4e101011c47ccc55a86d28c979a19ebcb92d1e`  
		Last Modified: Fri, 13 Oct 2023 20:50:41 GMT  
		Size: 5.0 MB (4982809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a18e8214bcecaf476164a2f5e27fbee68e657af02a45ccff4bec091d15044b`  
		Last Modified: Sat, 21 Oct 2023 00:30:30 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:9dce1c1ce729311280470aea6cb425a506188b2702ed1c75cda8e3f9ca2c36cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a859c2a13d0117b167ecf3c1130927b23abd6d788d55a2b26b35fd4d620be46`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:57:55 GMT
COPY file:5c489921e9dd684fb5e69dbf0d2c211653f6ca6b326f9f51a3f93f307aaf7808 in /nats-server 
# Fri, 27 Oct 2023 19:57:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:57:55 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:57:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:57:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e5204dbd51882e4867707ab178f23fd54d6c30e072917169c12a29fb29f2d900`  
		Last Modified: Fri, 27 Oct 2023 19:58:47 GMT  
		Size: 5.2 MB (5191456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc4cb991a069da2c550a4b4951d01811893ef1032980a277f673ca096b05c6b`  
		Last Modified: Fri, 27 Oct 2023 19:58:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:02c1d43c056e7545dc87e85ec89da70f4a39471f78470e2297cb49fc28ab360e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4976291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b087a7c300c290914637afef3115233ccf803a2325dbe358b1340ca32dd1bb2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 00:53:29 GMT
COPY file:c45665aaa0d25bdd0098d10b44c0de8efea234c8bb8ca8d2159b85284914acec in /nats-server 
# Sat, 21 Oct 2023 00:53:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 00:53:30 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 00:53:30 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 00:53:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a4d0acc6fe81e822f8d7b966098f56b50e69fda2eaab5ba79292315f68bc3a00`  
		Last Modified: Fri, 13 Oct 2023 20:59:06 GMT  
		Size: 5.0 MB (4975782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54dd2e715bf93536d4168ea488cb9fded424844d693c284f42fa19b1b4e70c7c`  
		Last Modified: Sat, 21 Oct 2023 00:54:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f547fa8c881d35fe2ec8d56a11fa32761085624a63e47624f20479a909f211a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5056051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c67a74cebb43fc4328a7683d38e1bcc0f30c2d603719c7e7f61c6c84353f53`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:40:19 GMT
COPY file:f0fa68e74def803c21b6f8269a3c75cd778bc42000a0681fcf1756130f3f8f0f in /nats-server 
# Fri, 27 Oct 2023 19:40:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:40:19 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:40:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:40:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ffe5996a38553f591ab54d703f3bbdb0cc32449b2ad8947b797aedbcfdb9ab7a`  
		Last Modified: Fri, 27 Oct 2023 19:41:06 GMT  
		Size: 5.1 MB (5055542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d3f38440ca89ef0ecab71a2f19751047fee6a0a5c7361057d77b22ef77bcc6`  
		Last Modified: Fri, 27 Oct 2023 19:41:05 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f98ebc31879e3e27bb8297d98564bf27d043c6c282b963c110467d1072e6d9f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4784170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658fcb0e4f11ac4f89b118f5c21a1de8336d063fc32f8f08f638ea8345617886`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 02:14:05 GMT
COPY file:75276c307f8eba0e9701c41a06bc7811acfb74142d0dee0a37dfb289dfda3db1 in /nats-server 
# Sat, 21 Oct 2023 02:14:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 02:14:05 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 02:14:05 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 02:14:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c50a270bdf1d14f1505fe9a625df2c74a90941d423db84eb62da12b3b6c813a4`  
		Last Modified: Fri, 13 Oct 2023 20:42:09 GMT  
		Size: 4.8 MB (4783661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4996d72414c18f73392ed69b9132989e283146fe606df3028fe2096bd633de`  
		Last Modified: Sat, 21 Oct 2023 02:15:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:29e2152405ed849d5c5589a35cf02b73576e88e08f0adf67040f458759dd892e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110065642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c710ddccc8cd69660a72c1525134e455f160899596c1a5f5155ce6f586ebdf7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 27 Oct 2023 20:17:42 GMT
RUN cmd /S /C #(nop) COPY file:18d2b201bedf44d6cf20990a5e1d83d3832eede6b2be4d6fa577c7cc28820bc5 in C:\nats-server.exe 
# Fri, 27 Oct 2023 20:17:43 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 Oct 2023 20:17:43 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 20:17:44 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 Oct 2023 20:17:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d2c4e1901a577a53d576303c5fb185d5d603a51a5963cce465f38722e9e7e3`  
		Last Modified: Fri, 27 Oct 2023 20:18:46 GMT  
		Size: 5.6 MB (5594656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:708131235a1cef76196cb5edbf912ebbc24020f96d3b0d168efe49cd88760665`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43906e90b84754a9e07f7b317810dec4106ba10d159dfe5bad8f536f9e8a376`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f4774c11b47cdb1c9434e6a07a055c33e201ece83051fd6bef2bcb38b955cb`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1c20f4d32a522c57acefece567048f4c290d4245799d7957e49dabe8bec88d`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:d21d20ce210a5b2ad455f59fb1575e46408b8f3412915236fb9e5b42e2409bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:e3dc3554afb54f24b96cc8b9ed45304e3cdf4af3e0d825513842cccc6443f850
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9507519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861b77f7441d4a0fb6c985252a186dd754c2bbfffb97adef86dfd317af118334`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:24:10 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:24:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:24:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:24:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:24:12 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:24:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:24:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f36f68f29c67409263076c2054d9e936c2f5e1a55ee937eb688ec1ce4915b8f`  
		Last Modified: Fri, 27 Oct 2023 19:25:16 GMT  
		Size: 6.1 MB (6104549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3bd88fc72377412d689508327b2bddbd4b2809fc079dfcead61801da1e9883c`  
		Last Modified: Fri, 27 Oct 2023 19:25:15 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29d0d1b8451bb92780ecfbc6b0f6488f2dbe6544277150975c6cfe9f22e12e3`  
		Last Modified: Fri, 27 Oct 2023 19:25:15 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:3f88f59fb120cd5be7f12dc9d2fb4b443ff7cd301e1bd95254dc57f4d2ce6561
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8970070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07efe60769658973f2765083517eda81ef09d5bb126a31af0295381865319ceb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:49:22 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:49:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:49:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:49:25 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:49:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a4fa6d23f1c5bfabc6eef228ba8baad859591a66d6499d64906f0f27f6d922`  
		Last Modified: Fri, 27 Oct 2023 19:50:04 GMT  
		Size: 5.8 MB (5823776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dfe6a1c19a37a61b685e720cd1156f95339fd4f9a4a425de2d8660166d9262e`  
		Last Modified: Fri, 27 Oct 2023 19:50:03 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3442d93fb16090b52375f2f415c787201447a8ade97b668a970f125f54a37e`  
		Last Modified: Fri, 27 Oct 2023 19:50:03 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:f38e6a15d5aee9730165a0a42dcaff9ecb306765613d8bab7eb1cfe51c7a306b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8714613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45868af98d7975ae09eecf8c1ad64a141d32fdb6a194bdf9afafffc05284c7c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:57:32 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:57:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:57:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:57:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:57:35 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:57:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:57:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44387fce322d8b03c5a038b2ba2a5e50919536ca64fd3fd32dddedce21340409`  
		Last Modified: Fri, 27 Oct 2023 19:58:22 GMT  
		Size: 5.8 MB (5813708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43c9b7450ee82499c6b877fa3b396205a7a4401978c9abd93e1b06200e9e5b0`  
		Last Modified: Fri, 27 Oct 2023 19:58:21 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59161e165420801f1ca6fba02cdfe0a8f3ba106b5443f1973c93063309ba83a`  
		Last Modified: Fri, 27 Oct 2023 19:58:21 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8b122cc94ebf709dd7ac8dbf611b3cbb93d995761f7a0cf90c9f1bfdc721db30
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9012372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1202aa9cd9cdcca825729430f679709284ca27900947697c866d1ced15ae5691`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:39:47 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:39:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:39:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:39:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:39:49 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:39:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:39:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b401e86e5d329ffd1a089932b1a9105a8375d0b413dc151add60434ed63162d1`  
		Last Modified: Fri, 27 Oct 2023 19:40:42 GMT  
		Size: 5.7 MB (5679544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939868b32dc69dc261c1c70fc9f1e9f3954f898d303b8d4a37e7178c8bf6c58b`  
		Last Modified: Fri, 27 Oct 2023 19:40:41 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b0ee4d1df33e3c8250ff7240533a3ea68875726979421fc6d9f705f0acf8d7`  
		Last Modified: Fri, 27 Oct 2023 19:40:41 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.18`

```console
$ docker pull nats@sha256:d21d20ce210a5b2ad455f59fb1575e46408b8f3412915236fb9e5b42e2409bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:e3dc3554afb54f24b96cc8b9ed45304e3cdf4af3e0d825513842cccc6443f850
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9507519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861b77f7441d4a0fb6c985252a186dd754c2bbfffb97adef86dfd317af118334`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:24:10 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:24:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:24:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:24:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:24:12 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:24:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:24:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f36f68f29c67409263076c2054d9e936c2f5e1a55ee937eb688ec1ce4915b8f`  
		Last Modified: Fri, 27 Oct 2023 19:25:16 GMT  
		Size: 6.1 MB (6104549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3bd88fc72377412d689508327b2bddbd4b2809fc079dfcead61801da1e9883c`  
		Last Modified: Fri, 27 Oct 2023 19:25:15 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29d0d1b8451bb92780ecfbc6b0f6488f2dbe6544277150975c6cfe9f22e12e3`  
		Last Modified: Fri, 27 Oct 2023 19:25:15 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:3f88f59fb120cd5be7f12dc9d2fb4b443ff7cd301e1bd95254dc57f4d2ce6561
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8970070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07efe60769658973f2765083517eda81ef09d5bb126a31af0295381865319ceb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:49:22 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:49:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:49:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:49:25 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:49:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a4fa6d23f1c5bfabc6eef228ba8baad859591a66d6499d64906f0f27f6d922`  
		Last Modified: Fri, 27 Oct 2023 19:50:04 GMT  
		Size: 5.8 MB (5823776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dfe6a1c19a37a61b685e720cd1156f95339fd4f9a4a425de2d8660166d9262e`  
		Last Modified: Fri, 27 Oct 2023 19:50:03 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3442d93fb16090b52375f2f415c787201447a8ade97b668a970f125f54a37e`  
		Last Modified: Fri, 27 Oct 2023 19:50:03 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:f38e6a15d5aee9730165a0a42dcaff9ecb306765613d8bab7eb1cfe51c7a306b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8714613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45868af98d7975ae09eecf8c1ad64a141d32fdb6a194bdf9afafffc05284c7c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:57:32 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:57:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:57:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:57:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:57:35 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:57:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:57:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44387fce322d8b03c5a038b2ba2a5e50919536ca64fd3fd32dddedce21340409`  
		Last Modified: Fri, 27 Oct 2023 19:58:22 GMT  
		Size: 5.8 MB (5813708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43c9b7450ee82499c6b877fa3b396205a7a4401978c9abd93e1b06200e9e5b0`  
		Last Modified: Fri, 27 Oct 2023 19:58:21 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59161e165420801f1ca6fba02cdfe0a8f3ba106b5443f1973c93063309ba83a`  
		Last Modified: Fri, 27 Oct 2023 19:58:21 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8b122cc94ebf709dd7ac8dbf611b3cbb93d995761f7a0cf90c9f1bfdc721db30
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9012372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1202aa9cd9cdcca825729430f679709284ca27900947697c866d1ced15ae5691`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:39:47 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:39:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:39:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:39:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:39:49 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:39:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:39:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b401e86e5d329ffd1a089932b1a9105a8375d0b413dc151add60434ed63162d1`  
		Last Modified: Fri, 27 Oct 2023 19:40:42 GMT  
		Size: 5.7 MB (5679544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939868b32dc69dc261c1c70fc9f1e9f3954f898d303b8d4a37e7178c8bf6c58b`  
		Last Modified: Fri, 27 Oct 2023 19:40:41 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b0ee4d1df33e3c8250ff7240533a3ea68875726979421fc6d9f705f0acf8d7`  
		Last Modified: Fri, 27 Oct 2023 19:40:41 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:4b0b2c55b843e8c73693a839f88d8e403414c171b5b109e3debd04b6a953f76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:fe0f6382b8b6b1820004268a1e539cabf394046302ddb9bd1fe14be1d5771fbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5481847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211d523019caad51116b188eb0cf75ce76becdb5aa40535a9f786d29130792f4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:24:45 GMT
COPY file:8488714a53ceca0afd69fdc135a2e59f81f3008e24d351a22438b39d8ab405fe in /nats-server 
# Fri, 27 Oct 2023 19:24:45 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:24:45 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:24:45 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:24:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:db9df0ffe6fe1654cbad22b0ee4be8b11d47faa0ee2c6f353915285f56329500`  
		Last Modified: Fri, 27 Oct 2023 19:25:41 GMT  
		Size: 5.5 MB (5481338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89fadd4ca8047bf736c814f88e92efa539731e382b4419dee4eee68edbe42fe`  
		Last Modified: Fri, 27 Oct 2023 19:25:40 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:b86c68503d84530fc3cb5ab2b6020dfe898e9e6d9b56965c14886b3cbdb07fd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5200382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7fef18696d3fe7987d9a9cbb167d045bcf97d5d2a1ac6fb76e73c65abde696`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:49:36 GMT
COPY file:0b4bcbfc47b21cd20c0f98a685ba4fbd4a6e7c8df6268e72fa48d2886a177781 in /nats-server 
# Fri, 27 Oct 2023 19:49:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:49:36 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:260eff5507dab2d5105a6c9ea84fc78fb51e66c5435f05572b8f8e7767cb103d`  
		Last Modified: Fri, 27 Oct 2023 19:50:29 GMT  
		Size: 5.2 MB (5199874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2e9e51baf6f1fddbeae98b8fed44bf52c3b147232cdea2f33fe5943fa9dc31`  
		Last Modified: Fri, 27 Oct 2023 19:50:28 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:9dce1c1ce729311280470aea6cb425a506188b2702ed1c75cda8e3f9ca2c36cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a859c2a13d0117b167ecf3c1130927b23abd6d788d55a2b26b35fd4d620be46`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:57:55 GMT
COPY file:5c489921e9dd684fb5e69dbf0d2c211653f6ca6b326f9f51a3f93f307aaf7808 in /nats-server 
# Fri, 27 Oct 2023 19:57:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:57:55 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:57:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:57:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e5204dbd51882e4867707ab178f23fd54d6c30e072917169c12a29fb29f2d900`  
		Last Modified: Fri, 27 Oct 2023 19:58:47 GMT  
		Size: 5.2 MB (5191456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc4cb991a069da2c550a4b4951d01811893ef1032980a277f673ca096b05c6b`  
		Last Modified: Fri, 27 Oct 2023 19:58:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f547fa8c881d35fe2ec8d56a11fa32761085624a63e47624f20479a909f211a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5056051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c67a74cebb43fc4328a7683d38e1bcc0f30c2d603719c7e7f61c6c84353f53`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:40:19 GMT
COPY file:f0fa68e74def803c21b6f8269a3c75cd778bc42000a0681fcf1756130f3f8f0f in /nats-server 
# Fri, 27 Oct 2023 19:40:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:40:19 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:40:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:40:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ffe5996a38553f591ab54d703f3bbdb0cc32449b2ad8947b797aedbcfdb9ab7a`  
		Last Modified: Fri, 27 Oct 2023 19:41:06 GMT  
		Size: 5.1 MB (5055542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d3f38440ca89ef0ecab71a2f19751047fee6a0a5c7361057d77b22ef77bcc6`  
		Last Modified: Fri, 27 Oct 2023 19:41:05 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:2dfff9132418c9602296d363dad4e205e785752d73ddca9f4537f91cd4db57c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:29e2152405ed849d5c5589a35cf02b73576e88e08f0adf67040f458759dd892e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110065642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c710ddccc8cd69660a72c1525134e455f160899596c1a5f5155ce6f586ebdf7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 27 Oct 2023 20:17:42 GMT
RUN cmd /S /C #(nop) COPY file:18d2b201bedf44d6cf20990a5e1d83d3832eede6b2be4d6fa577c7cc28820bc5 in C:\nats-server.exe 
# Fri, 27 Oct 2023 20:17:43 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 Oct 2023 20:17:43 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 20:17:44 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 Oct 2023 20:17:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d2c4e1901a577a53d576303c5fb185d5d603a51a5963cce465f38722e9e7e3`  
		Last Modified: Fri, 27 Oct 2023 20:18:46 GMT  
		Size: 5.6 MB (5594656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:708131235a1cef76196cb5edbf912ebbc24020f96d3b0d168efe49cd88760665`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43906e90b84754a9e07f7b317810dec4106ba10d159dfe5bad8f536f9e8a376`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f4774c11b47cdb1c9434e6a07a055c33e201ece83051fd6bef2bcb38b955cb`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1c20f4d32a522c57acefece567048f4c290d4245799d7957e49dabe8bec88d`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:2dfff9132418c9602296d363dad4e205e785752d73ddca9f4537f91cd4db57c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:29e2152405ed849d5c5589a35cf02b73576e88e08f0adf67040f458759dd892e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110065642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c710ddccc8cd69660a72c1525134e455f160899596c1a5f5155ce6f586ebdf7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 27 Oct 2023 20:17:42 GMT
RUN cmd /S /C #(nop) COPY file:18d2b201bedf44d6cf20990a5e1d83d3832eede6b2be4d6fa577c7cc28820bc5 in C:\nats-server.exe 
# Fri, 27 Oct 2023 20:17:43 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 Oct 2023 20:17:43 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 20:17:44 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 Oct 2023 20:17:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d2c4e1901a577a53d576303c5fb185d5d603a51a5963cce465f38722e9e7e3`  
		Last Modified: Fri, 27 Oct 2023 20:18:46 GMT  
		Size: 5.6 MB (5594656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:708131235a1cef76196cb5edbf912ebbc24020f96d3b0d168efe49cd88760665`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43906e90b84754a9e07f7b317810dec4106ba10d159dfe5bad8f536f9e8a376`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f4774c11b47cdb1c9434e6a07a055c33e201ece83051fd6bef2bcb38b955cb`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1c20f4d32a522c57acefece567048f4c290d4245799d7957e49dabe8bec88d`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:4b0b2c55b843e8c73693a839f88d8e403414c171b5b109e3debd04b6a953f76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:fe0f6382b8b6b1820004268a1e539cabf394046302ddb9bd1fe14be1d5771fbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5481847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211d523019caad51116b188eb0cf75ce76becdb5aa40535a9f786d29130792f4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:24:45 GMT
COPY file:8488714a53ceca0afd69fdc135a2e59f81f3008e24d351a22438b39d8ab405fe in /nats-server 
# Fri, 27 Oct 2023 19:24:45 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:24:45 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:24:45 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:24:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:db9df0ffe6fe1654cbad22b0ee4be8b11d47faa0ee2c6f353915285f56329500`  
		Last Modified: Fri, 27 Oct 2023 19:25:41 GMT  
		Size: 5.5 MB (5481338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89fadd4ca8047bf736c814f88e92efa539731e382b4419dee4eee68edbe42fe`  
		Last Modified: Fri, 27 Oct 2023 19:25:40 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:b86c68503d84530fc3cb5ab2b6020dfe898e9e6d9b56965c14886b3cbdb07fd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5200382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7fef18696d3fe7987d9a9cbb167d045bcf97d5d2a1ac6fb76e73c65abde696`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:49:36 GMT
COPY file:0b4bcbfc47b21cd20c0f98a685ba4fbd4a6e7c8df6268e72fa48d2886a177781 in /nats-server 
# Fri, 27 Oct 2023 19:49:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:49:36 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:260eff5507dab2d5105a6c9ea84fc78fb51e66c5435f05572b8f8e7767cb103d`  
		Last Modified: Fri, 27 Oct 2023 19:50:29 GMT  
		Size: 5.2 MB (5199874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2e9e51baf6f1fddbeae98b8fed44bf52c3b147232cdea2f33fe5943fa9dc31`  
		Last Modified: Fri, 27 Oct 2023 19:50:28 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:9dce1c1ce729311280470aea6cb425a506188b2702ed1c75cda8e3f9ca2c36cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a859c2a13d0117b167ecf3c1130927b23abd6d788d55a2b26b35fd4d620be46`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:57:55 GMT
COPY file:5c489921e9dd684fb5e69dbf0d2c211653f6ca6b326f9f51a3f93f307aaf7808 in /nats-server 
# Fri, 27 Oct 2023 19:57:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:57:55 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:57:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:57:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e5204dbd51882e4867707ab178f23fd54d6c30e072917169c12a29fb29f2d900`  
		Last Modified: Fri, 27 Oct 2023 19:58:47 GMT  
		Size: 5.2 MB (5191456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc4cb991a069da2c550a4b4951d01811893ef1032980a277f673ca096b05c6b`  
		Last Modified: Fri, 27 Oct 2023 19:58:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f547fa8c881d35fe2ec8d56a11fa32761085624a63e47624f20479a909f211a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5056051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c67a74cebb43fc4328a7683d38e1bcc0f30c2d603719c7e7f61c6c84353f53`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:40:19 GMT
COPY file:f0fa68e74def803c21b6f8269a3c75cd778bc42000a0681fcf1756130f3f8f0f in /nats-server 
# Fri, 27 Oct 2023 19:40:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:40:19 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:40:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:40:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ffe5996a38553f591ab54d703f3bbdb0cc32449b2ad8947b797aedbcfdb9ab7a`  
		Last Modified: Fri, 27 Oct 2023 19:41:06 GMT  
		Size: 5.1 MB (5055542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d3f38440ca89ef0ecab71a2f19751047fee6a0a5c7361057d77b22ef77bcc6`  
		Last Modified: Fri, 27 Oct 2023 19:41:05 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:77937863d60c0bd41b4552832c1e825585180192728ef72fada7e777025c53e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:4c07209387666f05878e9e5ae7b2ea5feabc48d1bec9b29529609573281e8b50
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2037948217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e9cdf75f9dd9ef8362501dca3e4ac1ac1fec7a948dbcf54f9a3381ba48425c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2023 03:32:17 GMT
ENV NATS_DOCKERIZED=1
# Fri, 27 Oct 2023 20:14:59 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 20:15:00 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.4/nats-server-v2.10.4-windows-amd64.zip
# Fri, 27 Oct 2023 20:15:00 GMT
ENV NATS_SERVER_SHASUM=8792f3578b6ba3c8f3fc7763da1aea0525e92a02657017831a7d14dfd86e4959
# Fri, 27 Oct 2023 20:15:56 GMT
RUN Set-PSDebug -Trace 2
# Fri, 27 Oct 2023 20:17:27 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 27 Oct 2023 20:17:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 Oct 2023 20:17:29 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 20:17:29 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 Oct 2023 20:17:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4919cd870c32d33d8113b108e3e6ea2391bbbc70b2cf7e9febeeee307b1a4`  
		Last Modified: Wed, 11 Oct 2023 03:40:35 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce27dbaad0cf1a29b13da65c8ec2c9e6b42aaf192bb7138ab6c5b740dbd77b05`  
		Last Modified: Wed, 11 Oct 2023 03:40:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeff23ed3e0ed1d47af9f5ba3e920f499df7461b6b573b9b8890894a817d4e75`  
		Last Modified: Fri, 27 Oct 2023 20:18:29 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687bf833004525211ca17823f9860a90dd003c3b892c5a408cea77feb2b2f657`  
		Last Modified: Fri, 27 Oct 2023 20:18:28 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e1e0eed1c2383c5f276e9864bae63d81808a836d2b5ad5809045ece6333d9d`  
		Last Modified: Fri, 27 Oct 2023 20:18:28 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0118469c9fe0e2307ec1b83c4d3be497c92225567d7442b8b4b146f077d6d248`  
		Last Modified: Fri, 27 Oct 2023 20:18:28 GMT  
		Size: 453.6 KB (453628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc366f4d0a9c64080edab305111762c36c9aae61164c3d341fe9354b6d2dd24c`  
		Last Modified: Fri, 27 Oct 2023 20:18:27 GMT  
		Size: 5.9 MB (5890774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca441f0e90699b8ec845791d94a479a4394595caaa203b5c46465e97b66039bf`  
		Last Modified: Fri, 27 Oct 2023 20:18:25 GMT  
		Size: 2.0 KB (1983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf52f2d7db58c482fbb66a79029866157c5109ebaa1502f55449091e1c2b4587`  
		Last Modified: Fri, 27 Oct 2023 20:18:25 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04b7cb73a561c0325b062bfd254f914ed85d7d87a33532704a94bdb95cf318e`  
		Last Modified: Fri, 27 Oct 2023 20:18:26 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c201e4889ec729fccadc69fde51e2dcb98d0ef71408c9b998cb0f0cd5737ef74`  
		Last Modified: Fri, 27 Oct 2023 20:18:26 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:77937863d60c0bd41b4552832c1e825585180192728ef72fada7e777025c53e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:4c07209387666f05878e9e5ae7b2ea5feabc48d1bec9b29529609573281e8b50
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2037948217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e9cdf75f9dd9ef8362501dca3e4ac1ac1fec7a948dbcf54f9a3381ba48425c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2023 03:32:17 GMT
ENV NATS_DOCKERIZED=1
# Fri, 27 Oct 2023 20:14:59 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 20:15:00 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.4/nats-server-v2.10.4-windows-amd64.zip
# Fri, 27 Oct 2023 20:15:00 GMT
ENV NATS_SERVER_SHASUM=8792f3578b6ba3c8f3fc7763da1aea0525e92a02657017831a7d14dfd86e4959
# Fri, 27 Oct 2023 20:15:56 GMT
RUN Set-PSDebug -Trace 2
# Fri, 27 Oct 2023 20:17:27 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 27 Oct 2023 20:17:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 Oct 2023 20:17:29 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 20:17:29 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 Oct 2023 20:17:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4919cd870c32d33d8113b108e3e6ea2391bbbc70b2cf7e9febeeee307b1a4`  
		Last Modified: Wed, 11 Oct 2023 03:40:35 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce27dbaad0cf1a29b13da65c8ec2c9e6b42aaf192bb7138ab6c5b740dbd77b05`  
		Last Modified: Wed, 11 Oct 2023 03:40:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeff23ed3e0ed1d47af9f5ba3e920f499df7461b6b573b9b8890894a817d4e75`  
		Last Modified: Fri, 27 Oct 2023 20:18:29 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687bf833004525211ca17823f9860a90dd003c3b892c5a408cea77feb2b2f657`  
		Last Modified: Fri, 27 Oct 2023 20:18:28 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e1e0eed1c2383c5f276e9864bae63d81808a836d2b5ad5809045ece6333d9d`  
		Last Modified: Fri, 27 Oct 2023 20:18:28 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0118469c9fe0e2307ec1b83c4d3be497c92225567d7442b8b4b146f077d6d248`  
		Last Modified: Fri, 27 Oct 2023 20:18:28 GMT  
		Size: 453.6 KB (453628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc366f4d0a9c64080edab305111762c36c9aae61164c3d341fe9354b6d2dd24c`  
		Last Modified: Fri, 27 Oct 2023 20:18:27 GMT  
		Size: 5.9 MB (5890774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca441f0e90699b8ec845791d94a479a4394595caaa203b5c46465e97b66039bf`  
		Last Modified: Fri, 27 Oct 2023 20:18:25 GMT  
		Size: 2.0 KB (1983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf52f2d7db58c482fbb66a79029866157c5109ebaa1502f55449091e1c2b4587`  
		Last Modified: Fri, 27 Oct 2023 20:18:25 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04b7cb73a561c0325b062bfd254f914ed85d7d87a33532704a94bdb95cf318e`  
		Last Modified: Fri, 27 Oct 2023 20:18:26 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c201e4889ec729fccadc69fde51e2dcb98d0ef71408c9b998cb0f0cd5737ef74`  
		Last Modified: Fri, 27 Oct 2023 20:18:26 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:6d3a6e5c9569cfd5063190bb86e48a51f6c3f728c615380bbe2ef67d0628055a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4974; amd64

### `nats:2.10` - linux; amd64

```console
$ docker pull nats@sha256:fe0f6382b8b6b1820004268a1e539cabf394046302ddb9bd1fe14be1d5771fbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5481847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211d523019caad51116b188eb0cf75ce76becdb5aa40535a9f786d29130792f4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:24:45 GMT
COPY file:8488714a53ceca0afd69fdc135a2e59f81f3008e24d351a22438b39d8ab405fe in /nats-server 
# Fri, 27 Oct 2023 19:24:45 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:24:45 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:24:45 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:24:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:db9df0ffe6fe1654cbad22b0ee4be8b11d47faa0ee2c6f353915285f56329500`  
		Last Modified: Fri, 27 Oct 2023 19:25:41 GMT  
		Size: 5.5 MB (5481338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89fadd4ca8047bf736c814f88e92efa539731e382b4419dee4eee68edbe42fe`  
		Last Modified: Fri, 27 Oct 2023 19:25:40 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:b86c68503d84530fc3cb5ab2b6020dfe898e9e6d9b56965c14886b3cbdb07fd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5200382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7fef18696d3fe7987d9a9cbb167d045bcf97d5d2a1ac6fb76e73c65abde696`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:49:36 GMT
COPY file:0b4bcbfc47b21cd20c0f98a685ba4fbd4a6e7c8df6268e72fa48d2886a177781 in /nats-server 
# Fri, 27 Oct 2023 19:49:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:49:36 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:260eff5507dab2d5105a6c9ea84fc78fb51e66c5435f05572b8f8e7767cb103d`  
		Last Modified: Fri, 27 Oct 2023 19:50:29 GMT  
		Size: 5.2 MB (5199874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2e9e51baf6f1fddbeae98b8fed44bf52c3b147232cdea2f33fe5943fa9dc31`  
		Last Modified: Fri, 27 Oct 2023 19:50:28 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:9dce1c1ce729311280470aea6cb425a506188b2702ed1c75cda8e3f9ca2c36cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a859c2a13d0117b167ecf3c1130927b23abd6d788d55a2b26b35fd4d620be46`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:57:55 GMT
COPY file:5c489921e9dd684fb5e69dbf0d2c211653f6ca6b326f9f51a3f93f307aaf7808 in /nats-server 
# Fri, 27 Oct 2023 19:57:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:57:55 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:57:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:57:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e5204dbd51882e4867707ab178f23fd54d6c30e072917169c12a29fb29f2d900`  
		Last Modified: Fri, 27 Oct 2023 19:58:47 GMT  
		Size: 5.2 MB (5191456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc4cb991a069da2c550a4b4951d01811893ef1032980a277f673ca096b05c6b`  
		Last Modified: Fri, 27 Oct 2023 19:58:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f547fa8c881d35fe2ec8d56a11fa32761085624a63e47624f20479a909f211a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5056051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c67a74cebb43fc4328a7683d38e1bcc0f30c2d603719c7e7f61c6c84353f53`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:40:19 GMT
COPY file:f0fa68e74def803c21b6f8269a3c75cd778bc42000a0681fcf1756130f3f8f0f in /nats-server 
# Fri, 27 Oct 2023 19:40:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:40:19 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:40:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:40:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ffe5996a38553f591ab54d703f3bbdb0cc32449b2ad8947b797aedbcfdb9ab7a`  
		Last Modified: Fri, 27 Oct 2023 19:41:06 GMT  
		Size: 5.1 MB (5055542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d3f38440ca89ef0ecab71a2f19751047fee6a0a5c7361057d77b22ef77bcc6`  
		Last Modified: Fri, 27 Oct 2023 19:41:05 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:29e2152405ed849d5c5589a35cf02b73576e88e08f0adf67040f458759dd892e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110065642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c710ddccc8cd69660a72c1525134e455f160899596c1a5f5155ce6f586ebdf7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 27 Oct 2023 20:17:42 GMT
RUN cmd /S /C #(nop) COPY file:18d2b201bedf44d6cf20990a5e1d83d3832eede6b2be4d6fa577c7cc28820bc5 in C:\nats-server.exe 
# Fri, 27 Oct 2023 20:17:43 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 Oct 2023 20:17:43 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 20:17:44 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 Oct 2023 20:17:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d2c4e1901a577a53d576303c5fb185d5d603a51a5963cce465f38722e9e7e3`  
		Last Modified: Fri, 27 Oct 2023 20:18:46 GMT  
		Size: 5.6 MB (5594656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:708131235a1cef76196cb5edbf912ebbc24020f96d3b0d168efe49cd88760665`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43906e90b84754a9e07f7b317810dec4106ba10d159dfe5bad8f536f9e8a376`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f4774c11b47cdb1c9434e6a07a055c33e201ece83051fd6bef2bcb38b955cb`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1c20f4d32a522c57acefece567048f4c290d4245799d7957e49dabe8bec88d`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:d21d20ce210a5b2ad455f59fb1575e46408b8f3412915236fb9e5b42e2409bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10-alpine` - linux; amd64

```console
$ docker pull nats@sha256:e3dc3554afb54f24b96cc8b9ed45304e3cdf4af3e0d825513842cccc6443f850
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9507519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861b77f7441d4a0fb6c985252a186dd754c2bbfffb97adef86dfd317af118334`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:24:10 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:24:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:24:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:24:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:24:12 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:24:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:24:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f36f68f29c67409263076c2054d9e936c2f5e1a55ee937eb688ec1ce4915b8f`  
		Last Modified: Fri, 27 Oct 2023 19:25:16 GMT  
		Size: 6.1 MB (6104549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3bd88fc72377412d689508327b2bddbd4b2809fc079dfcead61801da1e9883c`  
		Last Modified: Fri, 27 Oct 2023 19:25:15 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29d0d1b8451bb92780ecfbc6b0f6488f2dbe6544277150975c6cfe9f22e12e3`  
		Last Modified: Fri, 27 Oct 2023 19:25:15 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:3f88f59fb120cd5be7f12dc9d2fb4b443ff7cd301e1bd95254dc57f4d2ce6561
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8970070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07efe60769658973f2765083517eda81ef09d5bb126a31af0295381865319ceb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:49:22 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:49:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:49:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:49:25 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:49:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a4fa6d23f1c5bfabc6eef228ba8baad859591a66d6499d64906f0f27f6d922`  
		Last Modified: Fri, 27 Oct 2023 19:50:04 GMT  
		Size: 5.8 MB (5823776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dfe6a1c19a37a61b685e720cd1156f95339fd4f9a4a425de2d8660166d9262e`  
		Last Modified: Fri, 27 Oct 2023 19:50:03 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3442d93fb16090b52375f2f415c787201447a8ade97b668a970f125f54a37e`  
		Last Modified: Fri, 27 Oct 2023 19:50:03 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:f38e6a15d5aee9730165a0a42dcaff9ecb306765613d8bab7eb1cfe51c7a306b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8714613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45868af98d7975ae09eecf8c1ad64a141d32fdb6a194bdf9afafffc05284c7c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:57:32 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:57:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:57:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:57:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:57:35 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:57:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:57:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44387fce322d8b03c5a038b2ba2a5e50919536ca64fd3fd32dddedce21340409`  
		Last Modified: Fri, 27 Oct 2023 19:58:22 GMT  
		Size: 5.8 MB (5813708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43c9b7450ee82499c6b877fa3b396205a7a4401978c9abd93e1b06200e9e5b0`  
		Last Modified: Fri, 27 Oct 2023 19:58:21 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59161e165420801f1ca6fba02cdfe0a8f3ba106b5443f1973c93063309ba83a`  
		Last Modified: Fri, 27 Oct 2023 19:58:21 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8b122cc94ebf709dd7ac8dbf611b3cbb93d995761f7a0cf90c9f1bfdc721db30
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9012372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1202aa9cd9cdcca825729430f679709284ca27900947697c866d1ced15ae5691`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:39:47 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:39:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:39:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:39:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:39:49 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:39:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:39:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b401e86e5d329ffd1a089932b1a9105a8375d0b413dc151add60434ed63162d1`  
		Last Modified: Fri, 27 Oct 2023 19:40:42 GMT  
		Size: 5.7 MB (5679544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939868b32dc69dc261c1c70fc9f1e9f3954f898d303b8d4a37e7178c8bf6c58b`  
		Last Modified: Fri, 27 Oct 2023 19:40:41 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b0ee4d1df33e3c8250ff7240533a3ea68875726979421fc6d9f705f0acf8d7`  
		Last Modified: Fri, 27 Oct 2023 19:40:41 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine3.18`

```console
$ docker pull nats@sha256:d21d20ce210a5b2ad455f59fb1575e46408b8f3412915236fb9e5b42e2409bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:e3dc3554afb54f24b96cc8b9ed45304e3cdf4af3e0d825513842cccc6443f850
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9507519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861b77f7441d4a0fb6c985252a186dd754c2bbfffb97adef86dfd317af118334`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:24:10 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:24:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:24:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:24:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:24:12 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:24:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:24:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f36f68f29c67409263076c2054d9e936c2f5e1a55ee937eb688ec1ce4915b8f`  
		Last Modified: Fri, 27 Oct 2023 19:25:16 GMT  
		Size: 6.1 MB (6104549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3bd88fc72377412d689508327b2bddbd4b2809fc079dfcead61801da1e9883c`  
		Last Modified: Fri, 27 Oct 2023 19:25:15 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29d0d1b8451bb92780ecfbc6b0f6488f2dbe6544277150975c6cfe9f22e12e3`  
		Last Modified: Fri, 27 Oct 2023 19:25:15 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:3f88f59fb120cd5be7f12dc9d2fb4b443ff7cd301e1bd95254dc57f4d2ce6561
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8970070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07efe60769658973f2765083517eda81ef09d5bb126a31af0295381865319ceb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:49:22 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:49:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:49:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:49:25 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:49:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a4fa6d23f1c5bfabc6eef228ba8baad859591a66d6499d64906f0f27f6d922`  
		Last Modified: Fri, 27 Oct 2023 19:50:04 GMT  
		Size: 5.8 MB (5823776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dfe6a1c19a37a61b685e720cd1156f95339fd4f9a4a425de2d8660166d9262e`  
		Last Modified: Fri, 27 Oct 2023 19:50:03 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3442d93fb16090b52375f2f415c787201447a8ade97b668a970f125f54a37e`  
		Last Modified: Fri, 27 Oct 2023 19:50:03 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:f38e6a15d5aee9730165a0a42dcaff9ecb306765613d8bab7eb1cfe51c7a306b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8714613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45868af98d7975ae09eecf8c1ad64a141d32fdb6a194bdf9afafffc05284c7c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:57:32 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:57:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:57:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:57:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:57:35 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:57:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:57:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44387fce322d8b03c5a038b2ba2a5e50919536ca64fd3fd32dddedce21340409`  
		Last Modified: Fri, 27 Oct 2023 19:58:22 GMT  
		Size: 5.8 MB (5813708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43c9b7450ee82499c6b877fa3b396205a7a4401978c9abd93e1b06200e9e5b0`  
		Last Modified: Fri, 27 Oct 2023 19:58:21 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59161e165420801f1ca6fba02cdfe0a8f3ba106b5443f1973c93063309ba83a`  
		Last Modified: Fri, 27 Oct 2023 19:58:21 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8b122cc94ebf709dd7ac8dbf611b3cbb93d995761f7a0cf90c9f1bfdc721db30
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9012372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1202aa9cd9cdcca825729430f679709284ca27900947697c866d1ced15ae5691`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:39:47 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:39:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:39:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:39:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:39:49 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:39:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:39:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b401e86e5d329ffd1a089932b1a9105a8375d0b413dc151add60434ed63162d1`  
		Last Modified: Fri, 27 Oct 2023 19:40:42 GMT  
		Size: 5.7 MB (5679544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939868b32dc69dc261c1c70fc9f1e9f3954f898d303b8d4a37e7178c8bf6c58b`  
		Last Modified: Fri, 27 Oct 2023 19:40:41 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b0ee4d1df33e3c8250ff7240533a3ea68875726979421fc6d9f705f0acf8d7`  
		Last Modified: Fri, 27 Oct 2023 19:40:41 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:4b0b2c55b843e8c73693a839f88d8e403414c171b5b109e3debd04b6a953f76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10-linux` - linux; amd64

```console
$ docker pull nats@sha256:fe0f6382b8b6b1820004268a1e539cabf394046302ddb9bd1fe14be1d5771fbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5481847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211d523019caad51116b188eb0cf75ce76becdb5aa40535a9f786d29130792f4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:24:45 GMT
COPY file:8488714a53ceca0afd69fdc135a2e59f81f3008e24d351a22438b39d8ab405fe in /nats-server 
# Fri, 27 Oct 2023 19:24:45 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:24:45 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:24:45 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:24:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:db9df0ffe6fe1654cbad22b0ee4be8b11d47faa0ee2c6f353915285f56329500`  
		Last Modified: Fri, 27 Oct 2023 19:25:41 GMT  
		Size: 5.5 MB (5481338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89fadd4ca8047bf736c814f88e92efa539731e382b4419dee4eee68edbe42fe`  
		Last Modified: Fri, 27 Oct 2023 19:25:40 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:b86c68503d84530fc3cb5ab2b6020dfe898e9e6d9b56965c14886b3cbdb07fd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5200382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7fef18696d3fe7987d9a9cbb167d045bcf97d5d2a1ac6fb76e73c65abde696`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:49:36 GMT
COPY file:0b4bcbfc47b21cd20c0f98a685ba4fbd4a6e7c8df6268e72fa48d2886a177781 in /nats-server 
# Fri, 27 Oct 2023 19:49:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:49:36 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:260eff5507dab2d5105a6c9ea84fc78fb51e66c5435f05572b8f8e7767cb103d`  
		Last Modified: Fri, 27 Oct 2023 19:50:29 GMT  
		Size: 5.2 MB (5199874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2e9e51baf6f1fddbeae98b8fed44bf52c3b147232cdea2f33fe5943fa9dc31`  
		Last Modified: Fri, 27 Oct 2023 19:50:28 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:9dce1c1ce729311280470aea6cb425a506188b2702ed1c75cda8e3f9ca2c36cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a859c2a13d0117b167ecf3c1130927b23abd6d788d55a2b26b35fd4d620be46`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:57:55 GMT
COPY file:5c489921e9dd684fb5e69dbf0d2c211653f6ca6b326f9f51a3f93f307aaf7808 in /nats-server 
# Fri, 27 Oct 2023 19:57:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:57:55 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:57:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:57:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e5204dbd51882e4867707ab178f23fd54d6c30e072917169c12a29fb29f2d900`  
		Last Modified: Fri, 27 Oct 2023 19:58:47 GMT  
		Size: 5.2 MB (5191456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc4cb991a069da2c550a4b4951d01811893ef1032980a277f673ca096b05c6b`  
		Last Modified: Fri, 27 Oct 2023 19:58:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f547fa8c881d35fe2ec8d56a11fa32761085624a63e47624f20479a909f211a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5056051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c67a74cebb43fc4328a7683d38e1bcc0f30c2d603719c7e7f61c6c84353f53`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:40:19 GMT
COPY file:f0fa68e74def803c21b6f8269a3c75cd778bc42000a0681fcf1756130f3f8f0f in /nats-server 
# Fri, 27 Oct 2023 19:40:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:40:19 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:40:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:40:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ffe5996a38553f591ab54d703f3bbdb0cc32449b2ad8947b797aedbcfdb9ab7a`  
		Last Modified: Fri, 27 Oct 2023 19:41:06 GMT  
		Size: 5.1 MB (5055542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d3f38440ca89ef0ecab71a2f19751047fee6a0a5c7361057d77b22ef77bcc6`  
		Last Modified: Fri, 27 Oct 2023 19:41:05 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver`

```console
$ docker pull nats@sha256:2dfff9132418c9602296d363dad4e205e785752d73ddca9f4537f91cd4db57c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2.10-nanoserver` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:29e2152405ed849d5c5589a35cf02b73576e88e08f0adf67040f458759dd892e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110065642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c710ddccc8cd69660a72c1525134e455f160899596c1a5f5155ce6f586ebdf7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 27 Oct 2023 20:17:42 GMT
RUN cmd /S /C #(nop) COPY file:18d2b201bedf44d6cf20990a5e1d83d3832eede6b2be4d6fa577c7cc28820bc5 in C:\nats-server.exe 
# Fri, 27 Oct 2023 20:17:43 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 Oct 2023 20:17:43 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 20:17:44 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 Oct 2023 20:17:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d2c4e1901a577a53d576303c5fb185d5d603a51a5963cce465f38722e9e7e3`  
		Last Modified: Fri, 27 Oct 2023 20:18:46 GMT  
		Size: 5.6 MB (5594656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:708131235a1cef76196cb5edbf912ebbc24020f96d3b0d168efe49cd88760665`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43906e90b84754a9e07f7b317810dec4106ba10d159dfe5bad8f536f9e8a376`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f4774c11b47cdb1c9434e6a07a055c33e201ece83051fd6bef2bcb38b955cb`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1c20f4d32a522c57acefece567048f4c290d4245799d7957e49dabe8bec88d`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-1809`

```console
$ docker pull nats@sha256:2dfff9132418c9602296d363dad4e205e785752d73ddca9f4537f91cd4db57c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2.10-nanoserver-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:29e2152405ed849d5c5589a35cf02b73576e88e08f0adf67040f458759dd892e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110065642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c710ddccc8cd69660a72c1525134e455f160899596c1a5f5155ce6f586ebdf7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 27 Oct 2023 20:17:42 GMT
RUN cmd /S /C #(nop) COPY file:18d2b201bedf44d6cf20990a5e1d83d3832eede6b2be4d6fa577c7cc28820bc5 in C:\nats-server.exe 
# Fri, 27 Oct 2023 20:17:43 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 Oct 2023 20:17:43 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 20:17:44 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 Oct 2023 20:17:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d2c4e1901a577a53d576303c5fb185d5d603a51a5963cce465f38722e9e7e3`  
		Last Modified: Fri, 27 Oct 2023 20:18:46 GMT  
		Size: 5.6 MB (5594656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:708131235a1cef76196cb5edbf912ebbc24020f96d3b0d168efe49cd88760665`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43906e90b84754a9e07f7b317810dec4106ba10d159dfe5bad8f536f9e8a376`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f4774c11b47cdb1c9434e6a07a055c33e201ece83051fd6bef2bcb38b955cb`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1c20f4d32a522c57acefece567048f4c290d4245799d7957e49dabe8bec88d`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-scratch`

```console
$ docker pull nats@sha256:4b0b2c55b843e8c73693a839f88d8e403414c171b5b109e3debd04b6a953f76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10-scratch` - linux; amd64

```console
$ docker pull nats@sha256:fe0f6382b8b6b1820004268a1e539cabf394046302ddb9bd1fe14be1d5771fbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5481847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211d523019caad51116b188eb0cf75ce76becdb5aa40535a9f786d29130792f4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:24:45 GMT
COPY file:8488714a53ceca0afd69fdc135a2e59f81f3008e24d351a22438b39d8ab405fe in /nats-server 
# Fri, 27 Oct 2023 19:24:45 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:24:45 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:24:45 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:24:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:db9df0ffe6fe1654cbad22b0ee4be8b11d47faa0ee2c6f353915285f56329500`  
		Last Modified: Fri, 27 Oct 2023 19:25:41 GMT  
		Size: 5.5 MB (5481338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89fadd4ca8047bf736c814f88e92efa539731e382b4419dee4eee68edbe42fe`  
		Last Modified: Fri, 27 Oct 2023 19:25:40 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:b86c68503d84530fc3cb5ab2b6020dfe898e9e6d9b56965c14886b3cbdb07fd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5200382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7fef18696d3fe7987d9a9cbb167d045bcf97d5d2a1ac6fb76e73c65abde696`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:49:36 GMT
COPY file:0b4bcbfc47b21cd20c0f98a685ba4fbd4a6e7c8df6268e72fa48d2886a177781 in /nats-server 
# Fri, 27 Oct 2023 19:49:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:49:36 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:260eff5507dab2d5105a6c9ea84fc78fb51e66c5435f05572b8f8e7767cb103d`  
		Last Modified: Fri, 27 Oct 2023 19:50:29 GMT  
		Size: 5.2 MB (5199874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2e9e51baf6f1fddbeae98b8fed44bf52c3b147232cdea2f33fe5943fa9dc31`  
		Last Modified: Fri, 27 Oct 2023 19:50:28 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:9dce1c1ce729311280470aea6cb425a506188b2702ed1c75cda8e3f9ca2c36cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a859c2a13d0117b167ecf3c1130927b23abd6d788d55a2b26b35fd4d620be46`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:57:55 GMT
COPY file:5c489921e9dd684fb5e69dbf0d2c211653f6ca6b326f9f51a3f93f307aaf7808 in /nats-server 
# Fri, 27 Oct 2023 19:57:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:57:55 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:57:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:57:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e5204dbd51882e4867707ab178f23fd54d6c30e072917169c12a29fb29f2d900`  
		Last Modified: Fri, 27 Oct 2023 19:58:47 GMT  
		Size: 5.2 MB (5191456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc4cb991a069da2c550a4b4951d01811893ef1032980a277f673ca096b05c6b`  
		Last Modified: Fri, 27 Oct 2023 19:58:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f547fa8c881d35fe2ec8d56a11fa32761085624a63e47624f20479a909f211a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5056051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c67a74cebb43fc4328a7683d38e1bcc0f30c2d603719c7e7f61c6c84353f53`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:40:19 GMT
COPY file:f0fa68e74def803c21b6f8269a3c75cd778bc42000a0681fcf1756130f3f8f0f in /nats-server 
# Fri, 27 Oct 2023 19:40:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:40:19 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:40:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:40:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ffe5996a38553f591ab54d703f3bbdb0cc32449b2ad8947b797aedbcfdb9ab7a`  
		Last Modified: Fri, 27 Oct 2023 19:41:06 GMT  
		Size: 5.1 MB (5055542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d3f38440ca89ef0ecab71a2f19751047fee6a0a5c7361057d77b22ef77bcc6`  
		Last Modified: Fri, 27 Oct 2023 19:41:05 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore`

```console
$ docker pull nats@sha256:77937863d60c0bd41b4552832c1e825585180192728ef72fada7e777025c53e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:4c07209387666f05878e9e5ae7b2ea5feabc48d1bec9b29529609573281e8b50
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2037948217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e9cdf75f9dd9ef8362501dca3e4ac1ac1fec7a948dbcf54f9a3381ba48425c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2023 03:32:17 GMT
ENV NATS_DOCKERIZED=1
# Fri, 27 Oct 2023 20:14:59 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 20:15:00 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.4/nats-server-v2.10.4-windows-amd64.zip
# Fri, 27 Oct 2023 20:15:00 GMT
ENV NATS_SERVER_SHASUM=8792f3578b6ba3c8f3fc7763da1aea0525e92a02657017831a7d14dfd86e4959
# Fri, 27 Oct 2023 20:15:56 GMT
RUN Set-PSDebug -Trace 2
# Fri, 27 Oct 2023 20:17:27 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 27 Oct 2023 20:17:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 Oct 2023 20:17:29 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 20:17:29 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 Oct 2023 20:17:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4919cd870c32d33d8113b108e3e6ea2391bbbc70b2cf7e9febeeee307b1a4`  
		Last Modified: Wed, 11 Oct 2023 03:40:35 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce27dbaad0cf1a29b13da65c8ec2c9e6b42aaf192bb7138ab6c5b740dbd77b05`  
		Last Modified: Wed, 11 Oct 2023 03:40:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeff23ed3e0ed1d47af9f5ba3e920f499df7461b6b573b9b8890894a817d4e75`  
		Last Modified: Fri, 27 Oct 2023 20:18:29 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687bf833004525211ca17823f9860a90dd003c3b892c5a408cea77feb2b2f657`  
		Last Modified: Fri, 27 Oct 2023 20:18:28 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e1e0eed1c2383c5f276e9864bae63d81808a836d2b5ad5809045ece6333d9d`  
		Last Modified: Fri, 27 Oct 2023 20:18:28 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0118469c9fe0e2307ec1b83c4d3be497c92225567d7442b8b4b146f077d6d248`  
		Last Modified: Fri, 27 Oct 2023 20:18:28 GMT  
		Size: 453.6 KB (453628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc366f4d0a9c64080edab305111762c36c9aae61164c3d341fe9354b6d2dd24c`  
		Last Modified: Fri, 27 Oct 2023 20:18:27 GMT  
		Size: 5.9 MB (5890774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca441f0e90699b8ec845791d94a479a4394595caaa203b5c46465e97b66039bf`  
		Last Modified: Fri, 27 Oct 2023 20:18:25 GMT  
		Size: 2.0 KB (1983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf52f2d7db58c482fbb66a79029866157c5109ebaa1502f55449091e1c2b4587`  
		Last Modified: Fri, 27 Oct 2023 20:18:25 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04b7cb73a561c0325b062bfd254f914ed85d7d87a33532704a94bdb95cf318e`  
		Last Modified: Fri, 27 Oct 2023 20:18:26 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c201e4889ec729fccadc69fde51e2dcb98d0ef71408c9b998cb0f0cd5737ef74`  
		Last Modified: Fri, 27 Oct 2023 20:18:26 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-1809`

```console
$ docker pull nats@sha256:77937863d60c0bd41b4552832c1e825585180192728ef72fada7e777025c53e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2.10-windowsservercore-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:4c07209387666f05878e9e5ae7b2ea5feabc48d1bec9b29529609573281e8b50
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2037948217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e9cdf75f9dd9ef8362501dca3e4ac1ac1fec7a948dbcf54f9a3381ba48425c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2023 03:32:17 GMT
ENV NATS_DOCKERIZED=1
# Fri, 27 Oct 2023 20:14:59 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 20:15:00 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.4/nats-server-v2.10.4-windows-amd64.zip
# Fri, 27 Oct 2023 20:15:00 GMT
ENV NATS_SERVER_SHASUM=8792f3578b6ba3c8f3fc7763da1aea0525e92a02657017831a7d14dfd86e4959
# Fri, 27 Oct 2023 20:15:56 GMT
RUN Set-PSDebug -Trace 2
# Fri, 27 Oct 2023 20:17:27 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 27 Oct 2023 20:17:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 Oct 2023 20:17:29 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 20:17:29 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 Oct 2023 20:17:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4919cd870c32d33d8113b108e3e6ea2391bbbc70b2cf7e9febeeee307b1a4`  
		Last Modified: Wed, 11 Oct 2023 03:40:35 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce27dbaad0cf1a29b13da65c8ec2c9e6b42aaf192bb7138ab6c5b740dbd77b05`  
		Last Modified: Wed, 11 Oct 2023 03:40:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeff23ed3e0ed1d47af9f5ba3e920f499df7461b6b573b9b8890894a817d4e75`  
		Last Modified: Fri, 27 Oct 2023 20:18:29 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687bf833004525211ca17823f9860a90dd003c3b892c5a408cea77feb2b2f657`  
		Last Modified: Fri, 27 Oct 2023 20:18:28 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e1e0eed1c2383c5f276e9864bae63d81808a836d2b5ad5809045ece6333d9d`  
		Last Modified: Fri, 27 Oct 2023 20:18:28 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0118469c9fe0e2307ec1b83c4d3be497c92225567d7442b8b4b146f077d6d248`  
		Last Modified: Fri, 27 Oct 2023 20:18:28 GMT  
		Size: 453.6 KB (453628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc366f4d0a9c64080edab305111762c36c9aae61164c3d341fe9354b6d2dd24c`  
		Last Modified: Fri, 27 Oct 2023 20:18:27 GMT  
		Size: 5.9 MB (5890774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca441f0e90699b8ec845791d94a479a4394595caaa203b5c46465e97b66039bf`  
		Last Modified: Fri, 27 Oct 2023 20:18:25 GMT  
		Size: 2.0 KB (1983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf52f2d7db58c482fbb66a79029866157c5109ebaa1502f55449091e1c2b4587`  
		Last Modified: Fri, 27 Oct 2023 20:18:25 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04b7cb73a561c0325b062bfd254f914ed85d7d87a33532704a94bdb95cf318e`  
		Last Modified: Fri, 27 Oct 2023 20:18:26 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c201e4889ec729fccadc69fde51e2dcb98d0ef71408c9b998cb0f0cd5737ef74`  
		Last Modified: Fri, 27 Oct 2023 20:18:26 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.4`

```console
$ docker pull nats@sha256:6d3a6e5c9569cfd5063190bb86e48a51f6c3f728c615380bbe2ef67d0628055a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4974; amd64

### `nats:2.10.4` - linux; amd64

```console
$ docker pull nats@sha256:fe0f6382b8b6b1820004268a1e539cabf394046302ddb9bd1fe14be1d5771fbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5481847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211d523019caad51116b188eb0cf75ce76becdb5aa40535a9f786d29130792f4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:24:45 GMT
COPY file:8488714a53ceca0afd69fdc135a2e59f81f3008e24d351a22438b39d8ab405fe in /nats-server 
# Fri, 27 Oct 2023 19:24:45 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:24:45 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:24:45 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:24:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:db9df0ffe6fe1654cbad22b0ee4be8b11d47faa0ee2c6f353915285f56329500`  
		Last Modified: Fri, 27 Oct 2023 19:25:41 GMT  
		Size: 5.5 MB (5481338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89fadd4ca8047bf736c814f88e92efa539731e382b4419dee4eee68edbe42fe`  
		Last Modified: Fri, 27 Oct 2023 19:25:40 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.4` - linux; arm variant v6

```console
$ docker pull nats@sha256:b86c68503d84530fc3cb5ab2b6020dfe898e9e6d9b56965c14886b3cbdb07fd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5200382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7fef18696d3fe7987d9a9cbb167d045bcf97d5d2a1ac6fb76e73c65abde696`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:49:36 GMT
COPY file:0b4bcbfc47b21cd20c0f98a685ba4fbd4a6e7c8df6268e72fa48d2886a177781 in /nats-server 
# Fri, 27 Oct 2023 19:49:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:49:36 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:260eff5507dab2d5105a6c9ea84fc78fb51e66c5435f05572b8f8e7767cb103d`  
		Last Modified: Fri, 27 Oct 2023 19:50:29 GMT  
		Size: 5.2 MB (5199874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2e9e51baf6f1fddbeae98b8fed44bf52c3b147232cdea2f33fe5943fa9dc31`  
		Last Modified: Fri, 27 Oct 2023 19:50:28 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.4` - linux; arm variant v7

```console
$ docker pull nats@sha256:9dce1c1ce729311280470aea6cb425a506188b2702ed1c75cda8e3f9ca2c36cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a859c2a13d0117b167ecf3c1130927b23abd6d788d55a2b26b35fd4d620be46`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:57:55 GMT
COPY file:5c489921e9dd684fb5e69dbf0d2c211653f6ca6b326f9f51a3f93f307aaf7808 in /nats-server 
# Fri, 27 Oct 2023 19:57:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:57:55 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:57:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:57:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e5204dbd51882e4867707ab178f23fd54d6c30e072917169c12a29fb29f2d900`  
		Last Modified: Fri, 27 Oct 2023 19:58:47 GMT  
		Size: 5.2 MB (5191456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc4cb991a069da2c550a4b4951d01811893ef1032980a277f673ca096b05c6b`  
		Last Modified: Fri, 27 Oct 2023 19:58:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.4` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f547fa8c881d35fe2ec8d56a11fa32761085624a63e47624f20479a909f211a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5056051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c67a74cebb43fc4328a7683d38e1bcc0f30c2d603719c7e7f61c6c84353f53`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:40:19 GMT
COPY file:f0fa68e74def803c21b6f8269a3c75cd778bc42000a0681fcf1756130f3f8f0f in /nats-server 
# Fri, 27 Oct 2023 19:40:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:40:19 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:40:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:40:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ffe5996a38553f591ab54d703f3bbdb0cc32449b2ad8947b797aedbcfdb9ab7a`  
		Last Modified: Fri, 27 Oct 2023 19:41:06 GMT  
		Size: 5.1 MB (5055542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d3f38440ca89ef0ecab71a2f19751047fee6a0a5c7361057d77b22ef77bcc6`  
		Last Modified: Fri, 27 Oct 2023 19:41:05 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.4` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:29e2152405ed849d5c5589a35cf02b73576e88e08f0adf67040f458759dd892e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110065642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c710ddccc8cd69660a72c1525134e455f160899596c1a5f5155ce6f586ebdf7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 27 Oct 2023 20:17:42 GMT
RUN cmd /S /C #(nop) COPY file:18d2b201bedf44d6cf20990a5e1d83d3832eede6b2be4d6fa577c7cc28820bc5 in C:\nats-server.exe 
# Fri, 27 Oct 2023 20:17:43 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 Oct 2023 20:17:43 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 20:17:44 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 Oct 2023 20:17:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d2c4e1901a577a53d576303c5fb185d5d603a51a5963cce465f38722e9e7e3`  
		Last Modified: Fri, 27 Oct 2023 20:18:46 GMT  
		Size: 5.6 MB (5594656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:708131235a1cef76196cb5edbf912ebbc24020f96d3b0d168efe49cd88760665`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43906e90b84754a9e07f7b317810dec4106ba10d159dfe5bad8f536f9e8a376`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f4774c11b47cdb1c9434e6a07a055c33e201ece83051fd6bef2bcb38b955cb`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1c20f4d32a522c57acefece567048f4c290d4245799d7957e49dabe8bec88d`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.4-alpine`

```console
$ docker pull nats@sha256:d21d20ce210a5b2ad455f59fb1575e46408b8f3412915236fb9e5b42e2409bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10.4-alpine` - linux; amd64

```console
$ docker pull nats@sha256:e3dc3554afb54f24b96cc8b9ed45304e3cdf4af3e0d825513842cccc6443f850
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9507519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861b77f7441d4a0fb6c985252a186dd754c2bbfffb97adef86dfd317af118334`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:24:10 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:24:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:24:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:24:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:24:12 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:24:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:24:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f36f68f29c67409263076c2054d9e936c2f5e1a55ee937eb688ec1ce4915b8f`  
		Last Modified: Fri, 27 Oct 2023 19:25:16 GMT  
		Size: 6.1 MB (6104549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3bd88fc72377412d689508327b2bddbd4b2809fc079dfcead61801da1e9883c`  
		Last Modified: Fri, 27 Oct 2023 19:25:15 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29d0d1b8451bb92780ecfbc6b0f6488f2dbe6544277150975c6cfe9f22e12e3`  
		Last Modified: Fri, 27 Oct 2023 19:25:15 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.4-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:3f88f59fb120cd5be7f12dc9d2fb4b443ff7cd301e1bd95254dc57f4d2ce6561
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8970070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07efe60769658973f2765083517eda81ef09d5bb126a31af0295381865319ceb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:49:22 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:49:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:49:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:49:25 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:49:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a4fa6d23f1c5bfabc6eef228ba8baad859591a66d6499d64906f0f27f6d922`  
		Last Modified: Fri, 27 Oct 2023 19:50:04 GMT  
		Size: 5.8 MB (5823776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dfe6a1c19a37a61b685e720cd1156f95339fd4f9a4a425de2d8660166d9262e`  
		Last Modified: Fri, 27 Oct 2023 19:50:03 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3442d93fb16090b52375f2f415c787201447a8ade97b668a970f125f54a37e`  
		Last Modified: Fri, 27 Oct 2023 19:50:03 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.4-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:f38e6a15d5aee9730165a0a42dcaff9ecb306765613d8bab7eb1cfe51c7a306b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8714613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45868af98d7975ae09eecf8c1ad64a141d32fdb6a194bdf9afafffc05284c7c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:57:32 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:57:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:57:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:57:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:57:35 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:57:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:57:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44387fce322d8b03c5a038b2ba2a5e50919536ca64fd3fd32dddedce21340409`  
		Last Modified: Fri, 27 Oct 2023 19:58:22 GMT  
		Size: 5.8 MB (5813708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43c9b7450ee82499c6b877fa3b396205a7a4401978c9abd93e1b06200e9e5b0`  
		Last Modified: Fri, 27 Oct 2023 19:58:21 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59161e165420801f1ca6fba02cdfe0a8f3ba106b5443f1973c93063309ba83a`  
		Last Modified: Fri, 27 Oct 2023 19:58:21 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.4-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8b122cc94ebf709dd7ac8dbf611b3cbb93d995761f7a0cf90c9f1bfdc721db30
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9012372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1202aa9cd9cdcca825729430f679709284ca27900947697c866d1ced15ae5691`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:39:47 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:39:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:39:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:39:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:39:49 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:39:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:39:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b401e86e5d329ffd1a089932b1a9105a8375d0b413dc151add60434ed63162d1`  
		Last Modified: Fri, 27 Oct 2023 19:40:42 GMT  
		Size: 5.7 MB (5679544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939868b32dc69dc261c1c70fc9f1e9f3954f898d303b8d4a37e7178c8bf6c58b`  
		Last Modified: Fri, 27 Oct 2023 19:40:41 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b0ee4d1df33e3c8250ff7240533a3ea68875726979421fc6d9f705f0acf8d7`  
		Last Modified: Fri, 27 Oct 2023 19:40:41 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.4-alpine3.18`

```console
$ docker pull nats@sha256:d21d20ce210a5b2ad455f59fb1575e46408b8f3412915236fb9e5b42e2409bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10.4-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:e3dc3554afb54f24b96cc8b9ed45304e3cdf4af3e0d825513842cccc6443f850
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9507519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861b77f7441d4a0fb6c985252a186dd754c2bbfffb97adef86dfd317af118334`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:24:10 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:24:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:24:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:24:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:24:12 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:24:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:24:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f36f68f29c67409263076c2054d9e936c2f5e1a55ee937eb688ec1ce4915b8f`  
		Last Modified: Fri, 27 Oct 2023 19:25:16 GMT  
		Size: 6.1 MB (6104549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3bd88fc72377412d689508327b2bddbd4b2809fc079dfcead61801da1e9883c`  
		Last Modified: Fri, 27 Oct 2023 19:25:15 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29d0d1b8451bb92780ecfbc6b0f6488f2dbe6544277150975c6cfe9f22e12e3`  
		Last Modified: Fri, 27 Oct 2023 19:25:15 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.4-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:3f88f59fb120cd5be7f12dc9d2fb4b443ff7cd301e1bd95254dc57f4d2ce6561
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8970070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07efe60769658973f2765083517eda81ef09d5bb126a31af0295381865319ceb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:49:22 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:49:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:49:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:49:25 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:49:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a4fa6d23f1c5bfabc6eef228ba8baad859591a66d6499d64906f0f27f6d922`  
		Last Modified: Fri, 27 Oct 2023 19:50:04 GMT  
		Size: 5.8 MB (5823776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dfe6a1c19a37a61b685e720cd1156f95339fd4f9a4a425de2d8660166d9262e`  
		Last Modified: Fri, 27 Oct 2023 19:50:03 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3442d93fb16090b52375f2f415c787201447a8ade97b668a970f125f54a37e`  
		Last Modified: Fri, 27 Oct 2023 19:50:03 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.4-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:f38e6a15d5aee9730165a0a42dcaff9ecb306765613d8bab7eb1cfe51c7a306b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8714613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45868af98d7975ae09eecf8c1ad64a141d32fdb6a194bdf9afafffc05284c7c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:57:32 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:57:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:57:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:57:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:57:35 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:57:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:57:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44387fce322d8b03c5a038b2ba2a5e50919536ca64fd3fd32dddedce21340409`  
		Last Modified: Fri, 27 Oct 2023 19:58:22 GMT  
		Size: 5.8 MB (5813708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43c9b7450ee82499c6b877fa3b396205a7a4401978c9abd93e1b06200e9e5b0`  
		Last Modified: Fri, 27 Oct 2023 19:58:21 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59161e165420801f1ca6fba02cdfe0a8f3ba106b5443f1973c93063309ba83a`  
		Last Modified: Fri, 27 Oct 2023 19:58:21 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.4-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8b122cc94ebf709dd7ac8dbf611b3cbb93d995761f7a0cf90c9f1bfdc721db30
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9012372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1202aa9cd9cdcca825729430f679709284ca27900947697c866d1ced15ae5691`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:39:47 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:39:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:39:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:39:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:39:49 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:39:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:39:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b401e86e5d329ffd1a089932b1a9105a8375d0b413dc151add60434ed63162d1`  
		Last Modified: Fri, 27 Oct 2023 19:40:42 GMT  
		Size: 5.7 MB (5679544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939868b32dc69dc261c1c70fc9f1e9f3954f898d303b8d4a37e7178c8bf6c58b`  
		Last Modified: Fri, 27 Oct 2023 19:40:41 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b0ee4d1df33e3c8250ff7240533a3ea68875726979421fc6d9f705f0acf8d7`  
		Last Modified: Fri, 27 Oct 2023 19:40:41 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.4-linux`

```console
$ docker pull nats@sha256:4b0b2c55b843e8c73693a839f88d8e403414c171b5b109e3debd04b6a953f76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10.4-linux` - linux; amd64

```console
$ docker pull nats@sha256:fe0f6382b8b6b1820004268a1e539cabf394046302ddb9bd1fe14be1d5771fbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5481847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211d523019caad51116b188eb0cf75ce76becdb5aa40535a9f786d29130792f4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:24:45 GMT
COPY file:8488714a53ceca0afd69fdc135a2e59f81f3008e24d351a22438b39d8ab405fe in /nats-server 
# Fri, 27 Oct 2023 19:24:45 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:24:45 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:24:45 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:24:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:db9df0ffe6fe1654cbad22b0ee4be8b11d47faa0ee2c6f353915285f56329500`  
		Last Modified: Fri, 27 Oct 2023 19:25:41 GMT  
		Size: 5.5 MB (5481338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89fadd4ca8047bf736c814f88e92efa539731e382b4419dee4eee68edbe42fe`  
		Last Modified: Fri, 27 Oct 2023 19:25:40 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.4-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:b86c68503d84530fc3cb5ab2b6020dfe898e9e6d9b56965c14886b3cbdb07fd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5200382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7fef18696d3fe7987d9a9cbb167d045bcf97d5d2a1ac6fb76e73c65abde696`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:49:36 GMT
COPY file:0b4bcbfc47b21cd20c0f98a685ba4fbd4a6e7c8df6268e72fa48d2886a177781 in /nats-server 
# Fri, 27 Oct 2023 19:49:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:49:36 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:260eff5507dab2d5105a6c9ea84fc78fb51e66c5435f05572b8f8e7767cb103d`  
		Last Modified: Fri, 27 Oct 2023 19:50:29 GMT  
		Size: 5.2 MB (5199874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2e9e51baf6f1fddbeae98b8fed44bf52c3b147232cdea2f33fe5943fa9dc31`  
		Last Modified: Fri, 27 Oct 2023 19:50:28 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.4-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:9dce1c1ce729311280470aea6cb425a506188b2702ed1c75cda8e3f9ca2c36cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a859c2a13d0117b167ecf3c1130927b23abd6d788d55a2b26b35fd4d620be46`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:57:55 GMT
COPY file:5c489921e9dd684fb5e69dbf0d2c211653f6ca6b326f9f51a3f93f307aaf7808 in /nats-server 
# Fri, 27 Oct 2023 19:57:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:57:55 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:57:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:57:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e5204dbd51882e4867707ab178f23fd54d6c30e072917169c12a29fb29f2d900`  
		Last Modified: Fri, 27 Oct 2023 19:58:47 GMT  
		Size: 5.2 MB (5191456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc4cb991a069da2c550a4b4951d01811893ef1032980a277f673ca096b05c6b`  
		Last Modified: Fri, 27 Oct 2023 19:58:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.4-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f547fa8c881d35fe2ec8d56a11fa32761085624a63e47624f20479a909f211a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5056051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c67a74cebb43fc4328a7683d38e1bcc0f30c2d603719c7e7f61c6c84353f53`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:40:19 GMT
COPY file:f0fa68e74def803c21b6f8269a3c75cd778bc42000a0681fcf1756130f3f8f0f in /nats-server 
# Fri, 27 Oct 2023 19:40:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:40:19 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:40:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:40:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ffe5996a38553f591ab54d703f3bbdb0cc32449b2ad8947b797aedbcfdb9ab7a`  
		Last Modified: Fri, 27 Oct 2023 19:41:06 GMT  
		Size: 5.1 MB (5055542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d3f38440ca89ef0ecab71a2f19751047fee6a0a5c7361057d77b22ef77bcc6`  
		Last Modified: Fri, 27 Oct 2023 19:41:05 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.4-nanoserver`

```console
$ docker pull nats@sha256:2dfff9132418c9602296d363dad4e205e785752d73ddca9f4537f91cd4db57c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2.10.4-nanoserver` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:29e2152405ed849d5c5589a35cf02b73576e88e08f0adf67040f458759dd892e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110065642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c710ddccc8cd69660a72c1525134e455f160899596c1a5f5155ce6f586ebdf7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 27 Oct 2023 20:17:42 GMT
RUN cmd /S /C #(nop) COPY file:18d2b201bedf44d6cf20990a5e1d83d3832eede6b2be4d6fa577c7cc28820bc5 in C:\nats-server.exe 
# Fri, 27 Oct 2023 20:17:43 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 Oct 2023 20:17:43 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 20:17:44 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 Oct 2023 20:17:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d2c4e1901a577a53d576303c5fb185d5d603a51a5963cce465f38722e9e7e3`  
		Last Modified: Fri, 27 Oct 2023 20:18:46 GMT  
		Size: 5.6 MB (5594656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:708131235a1cef76196cb5edbf912ebbc24020f96d3b0d168efe49cd88760665`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43906e90b84754a9e07f7b317810dec4106ba10d159dfe5bad8f536f9e8a376`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f4774c11b47cdb1c9434e6a07a055c33e201ece83051fd6bef2bcb38b955cb`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1c20f4d32a522c57acefece567048f4c290d4245799d7957e49dabe8bec88d`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.4-nanoserver-1809`

```console
$ docker pull nats@sha256:2dfff9132418c9602296d363dad4e205e785752d73ddca9f4537f91cd4db57c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2.10.4-nanoserver-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:29e2152405ed849d5c5589a35cf02b73576e88e08f0adf67040f458759dd892e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110065642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c710ddccc8cd69660a72c1525134e455f160899596c1a5f5155ce6f586ebdf7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 27 Oct 2023 20:17:42 GMT
RUN cmd /S /C #(nop) COPY file:18d2b201bedf44d6cf20990a5e1d83d3832eede6b2be4d6fa577c7cc28820bc5 in C:\nats-server.exe 
# Fri, 27 Oct 2023 20:17:43 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 Oct 2023 20:17:43 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 20:17:44 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 Oct 2023 20:17:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d2c4e1901a577a53d576303c5fb185d5d603a51a5963cce465f38722e9e7e3`  
		Last Modified: Fri, 27 Oct 2023 20:18:46 GMT  
		Size: 5.6 MB (5594656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:708131235a1cef76196cb5edbf912ebbc24020f96d3b0d168efe49cd88760665`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43906e90b84754a9e07f7b317810dec4106ba10d159dfe5bad8f536f9e8a376`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f4774c11b47cdb1c9434e6a07a055c33e201ece83051fd6bef2bcb38b955cb`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1c20f4d32a522c57acefece567048f4c290d4245799d7957e49dabe8bec88d`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.4-scratch`

```console
$ docker pull nats@sha256:4b0b2c55b843e8c73693a839f88d8e403414c171b5b109e3debd04b6a953f76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10.4-scratch` - linux; amd64

```console
$ docker pull nats@sha256:fe0f6382b8b6b1820004268a1e539cabf394046302ddb9bd1fe14be1d5771fbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5481847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211d523019caad51116b188eb0cf75ce76becdb5aa40535a9f786d29130792f4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:24:45 GMT
COPY file:8488714a53ceca0afd69fdc135a2e59f81f3008e24d351a22438b39d8ab405fe in /nats-server 
# Fri, 27 Oct 2023 19:24:45 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:24:45 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:24:45 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:24:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:db9df0ffe6fe1654cbad22b0ee4be8b11d47faa0ee2c6f353915285f56329500`  
		Last Modified: Fri, 27 Oct 2023 19:25:41 GMT  
		Size: 5.5 MB (5481338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89fadd4ca8047bf736c814f88e92efa539731e382b4419dee4eee68edbe42fe`  
		Last Modified: Fri, 27 Oct 2023 19:25:40 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.4-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:b86c68503d84530fc3cb5ab2b6020dfe898e9e6d9b56965c14886b3cbdb07fd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5200382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7fef18696d3fe7987d9a9cbb167d045bcf97d5d2a1ac6fb76e73c65abde696`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:49:36 GMT
COPY file:0b4bcbfc47b21cd20c0f98a685ba4fbd4a6e7c8df6268e72fa48d2886a177781 in /nats-server 
# Fri, 27 Oct 2023 19:49:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:49:36 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:260eff5507dab2d5105a6c9ea84fc78fb51e66c5435f05572b8f8e7767cb103d`  
		Last Modified: Fri, 27 Oct 2023 19:50:29 GMT  
		Size: 5.2 MB (5199874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2e9e51baf6f1fddbeae98b8fed44bf52c3b147232cdea2f33fe5943fa9dc31`  
		Last Modified: Fri, 27 Oct 2023 19:50:28 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.4-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:9dce1c1ce729311280470aea6cb425a506188b2702ed1c75cda8e3f9ca2c36cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a859c2a13d0117b167ecf3c1130927b23abd6d788d55a2b26b35fd4d620be46`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:57:55 GMT
COPY file:5c489921e9dd684fb5e69dbf0d2c211653f6ca6b326f9f51a3f93f307aaf7808 in /nats-server 
# Fri, 27 Oct 2023 19:57:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:57:55 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:57:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:57:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e5204dbd51882e4867707ab178f23fd54d6c30e072917169c12a29fb29f2d900`  
		Last Modified: Fri, 27 Oct 2023 19:58:47 GMT  
		Size: 5.2 MB (5191456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc4cb991a069da2c550a4b4951d01811893ef1032980a277f673ca096b05c6b`  
		Last Modified: Fri, 27 Oct 2023 19:58:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.4-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f547fa8c881d35fe2ec8d56a11fa32761085624a63e47624f20479a909f211a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5056051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c67a74cebb43fc4328a7683d38e1bcc0f30c2d603719c7e7f61c6c84353f53`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:40:19 GMT
COPY file:f0fa68e74def803c21b6f8269a3c75cd778bc42000a0681fcf1756130f3f8f0f in /nats-server 
# Fri, 27 Oct 2023 19:40:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:40:19 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:40:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:40:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ffe5996a38553f591ab54d703f3bbdb0cc32449b2ad8947b797aedbcfdb9ab7a`  
		Last Modified: Fri, 27 Oct 2023 19:41:06 GMT  
		Size: 5.1 MB (5055542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d3f38440ca89ef0ecab71a2f19751047fee6a0a5c7361057d77b22ef77bcc6`  
		Last Modified: Fri, 27 Oct 2023 19:41:05 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.4-windowsservercore`

```console
$ docker pull nats@sha256:77937863d60c0bd41b4552832c1e825585180192728ef72fada7e777025c53e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2.10.4-windowsservercore` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:4c07209387666f05878e9e5ae7b2ea5feabc48d1bec9b29529609573281e8b50
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2037948217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e9cdf75f9dd9ef8362501dca3e4ac1ac1fec7a948dbcf54f9a3381ba48425c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2023 03:32:17 GMT
ENV NATS_DOCKERIZED=1
# Fri, 27 Oct 2023 20:14:59 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 20:15:00 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.4/nats-server-v2.10.4-windows-amd64.zip
# Fri, 27 Oct 2023 20:15:00 GMT
ENV NATS_SERVER_SHASUM=8792f3578b6ba3c8f3fc7763da1aea0525e92a02657017831a7d14dfd86e4959
# Fri, 27 Oct 2023 20:15:56 GMT
RUN Set-PSDebug -Trace 2
# Fri, 27 Oct 2023 20:17:27 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 27 Oct 2023 20:17:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 Oct 2023 20:17:29 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 20:17:29 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 Oct 2023 20:17:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4919cd870c32d33d8113b108e3e6ea2391bbbc70b2cf7e9febeeee307b1a4`  
		Last Modified: Wed, 11 Oct 2023 03:40:35 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce27dbaad0cf1a29b13da65c8ec2c9e6b42aaf192bb7138ab6c5b740dbd77b05`  
		Last Modified: Wed, 11 Oct 2023 03:40:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeff23ed3e0ed1d47af9f5ba3e920f499df7461b6b573b9b8890894a817d4e75`  
		Last Modified: Fri, 27 Oct 2023 20:18:29 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687bf833004525211ca17823f9860a90dd003c3b892c5a408cea77feb2b2f657`  
		Last Modified: Fri, 27 Oct 2023 20:18:28 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e1e0eed1c2383c5f276e9864bae63d81808a836d2b5ad5809045ece6333d9d`  
		Last Modified: Fri, 27 Oct 2023 20:18:28 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0118469c9fe0e2307ec1b83c4d3be497c92225567d7442b8b4b146f077d6d248`  
		Last Modified: Fri, 27 Oct 2023 20:18:28 GMT  
		Size: 453.6 KB (453628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc366f4d0a9c64080edab305111762c36c9aae61164c3d341fe9354b6d2dd24c`  
		Last Modified: Fri, 27 Oct 2023 20:18:27 GMT  
		Size: 5.9 MB (5890774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca441f0e90699b8ec845791d94a479a4394595caaa203b5c46465e97b66039bf`  
		Last Modified: Fri, 27 Oct 2023 20:18:25 GMT  
		Size: 2.0 KB (1983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf52f2d7db58c482fbb66a79029866157c5109ebaa1502f55449091e1c2b4587`  
		Last Modified: Fri, 27 Oct 2023 20:18:25 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04b7cb73a561c0325b062bfd254f914ed85d7d87a33532704a94bdb95cf318e`  
		Last Modified: Fri, 27 Oct 2023 20:18:26 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c201e4889ec729fccadc69fde51e2dcb98d0ef71408c9b998cb0f0cd5737ef74`  
		Last Modified: Fri, 27 Oct 2023 20:18:26 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.4-windowsservercore-1809`

```console
$ docker pull nats@sha256:77937863d60c0bd41b4552832c1e825585180192728ef72fada7e777025c53e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2.10.4-windowsservercore-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:4c07209387666f05878e9e5ae7b2ea5feabc48d1bec9b29529609573281e8b50
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2037948217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e9cdf75f9dd9ef8362501dca3e4ac1ac1fec7a948dbcf54f9a3381ba48425c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2023 03:32:17 GMT
ENV NATS_DOCKERIZED=1
# Fri, 27 Oct 2023 20:14:59 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 20:15:00 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.4/nats-server-v2.10.4-windows-amd64.zip
# Fri, 27 Oct 2023 20:15:00 GMT
ENV NATS_SERVER_SHASUM=8792f3578b6ba3c8f3fc7763da1aea0525e92a02657017831a7d14dfd86e4959
# Fri, 27 Oct 2023 20:15:56 GMT
RUN Set-PSDebug -Trace 2
# Fri, 27 Oct 2023 20:17:27 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 27 Oct 2023 20:17:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 Oct 2023 20:17:29 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 20:17:29 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 Oct 2023 20:17:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4919cd870c32d33d8113b108e3e6ea2391bbbc70b2cf7e9febeeee307b1a4`  
		Last Modified: Wed, 11 Oct 2023 03:40:35 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce27dbaad0cf1a29b13da65c8ec2c9e6b42aaf192bb7138ab6c5b740dbd77b05`  
		Last Modified: Wed, 11 Oct 2023 03:40:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeff23ed3e0ed1d47af9f5ba3e920f499df7461b6b573b9b8890894a817d4e75`  
		Last Modified: Fri, 27 Oct 2023 20:18:29 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687bf833004525211ca17823f9860a90dd003c3b892c5a408cea77feb2b2f657`  
		Last Modified: Fri, 27 Oct 2023 20:18:28 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e1e0eed1c2383c5f276e9864bae63d81808a836d2b5ad5809045ece6333d9d`  
		Last Modified: Fri, 27 Oct 2023 20:18:28 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0118469c9fe0e2307ec1b83c4d3be497c92225567d7442b8b4b146f077d6d248`  
		Last Modified: Fri, 27 Oct 2023 20:18:28 GMT  
		Size: 453.6 KB (453628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc366f4d0a9c64080edab305111762c36c9aae61164c3d341fe9354b6d2dd24c`  
		Last Modified: Fri, 27 Oct 2023 20:18:27 GMT  
		Size: 5.9 MB (5890774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca441f0e90699b8ec845791d94a479a4394595caaa203b5c46465e97b66039bf`  
		Last Modified: Fri, 27 Oct 2023 20:18:25 GMT  
		Size: 2.0 KB (1983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf52f2d7db58c482fbb66a79029866157c5109ebaa1502f55449091e1c2b4587`  
		Last Modified: Fri, 27 Oct 2023 20:18:25 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04b7cb73a561c0325b062bfd254f914ed85d7d87a33532704a94bdb95cf318e`  
		Last Modified: Fri, 27 Oct 2023 20:18:26 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c201e4889ec729fccadc69fde51e2dcb98d0ef71408c9b998cb0f0cd5737ef74`  
		Last Modified: Fri, 27 Oct 2023 20:18:26 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9`

```console
$ docker pull nats@sha256:f6eba7c6befccb26620202fbe389fec5f159cd8ff08f6c716ad59f1cb6ce1d84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9` - linux; amd64

```console
$ docker pull nats@sha256:7d149a46fee148c37fa3b2bca97ac72ab1f96ed1793f8114cfecb40adc754119
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5247112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d7fa3037dc87b27de3f83d3dcb521067502705385f652d472d31fa037af822`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 02:39:39 GMT
COPY file:71487567f54b75938083a2680d411bd9e194b037c12b743a3c280c58abd7e82f in /nats-server 
# Sat, 21 Oct 2023 02:39:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 02:39:39 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 02:39:40 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 02:39:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5d153758a0dd20c137d358179ec27f8aca298056d0b26005f90208c882f0c7fa`  
		Last Modified: Fri, 13 Oct 2023 20:22:03 GMT  
		Size: 5.2 MB (5246604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e10c8d3bbc8928c41b93c6acf289f4b157e058ca08c00bee7222d13f60ce5b`  
		Last Modified: Sat, 21 Oct 2023 02:40:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v6

```console
$ docker pull nats@sha256:e80d5b10ed40caa3cae83ffa38af5ef4bb0c64e0a2174439dac89888d070cfc3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4983318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f65e0f853a25dd0c5e95c7b124ee834aafd668a27728562f5992e6bf60bce3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 00:29:27 GMT
COPY file:a99ff6735b1292770195e5dfe0e7f8a56bae939bfb272c8cbdfb47e7ba6c4828 in /nats-server 
# Sat, 21 Oct 2023 00:29:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 00:29:27 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 00:29:27 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 00:29:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:217c24d6cc08c267f56e5da2ce4e101011c47ccc55a86d28c979a19ebcb92d1e`  
		Last Modified: Fri, 13 Oct 2023 20:50:41 GMT  
		Size: 5.0 MB (4982809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a18e8214bcecaf476164a2f5e27fbee68e657af02a45ccff4bec091d15044b`  
		Last Modified: Sat, 21 Oct 2023 00:30:30 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v7

```console
$ docker pull nats@sha256:02c1d43c056e7545dc87e85ec89da70f4a39471f78470e2297cb49fc28ab360e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4976291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b087a7c300c290914637afef3115233ccf803a2325dbe358b1340ca32dd1bb2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 00:53:29 GMT
COPY file:c45665aaa0d25bdd0098d10b44c0de8efea234c8bb8ca8d2159b85284914acec in /nats-server 
# Sat, 21 Oct 2023 00:53:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 00:53:30 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 00:53:30 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 00:53:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a4d0acc6fe81e822f8d7b966098f56b50e69fda2eaab5ba79292315f68bc3a00`  
		Last Modified: Fri, 13 Oct 2023 20:59:06 GMT  
		Size: 5.0 MB (4975782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54dd2e715bf93536d4168ea488cb9fded424844d693c284f42fa19b1b4e70c7c`  
		Last Modified: Sat, 21 Oct 2023 00:54:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f98ebc31879e3e27bb8297d98564bf27d043c6c282b963c110467d1072e6d9f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4784170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658fcb0e4f11ac4f89b118f5c21a1de8336d063fc32f8f08f638ea8345617886`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 02:14:05 GMT
COPY file:75276c307f8eba0e9701c41a06bc7811acfb74142d0dee0a37dfb289dfda3db1 in /nats-server 
# Sat, 21 Oct 2023 02:14:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 02:14:05 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 02:14:05 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 02:14:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c50a270bdf1d14f1505fe9a625df2c74a90941d423db84eb62da12b3b6c813a4`  
		Last Modified: Fri, 13 Oct 2023 20:42:09 GMT  
		Size: 4.8 MB (4783661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4996d72414c18f73392ed69b9132989e283146fe606df3028fe2096bd633de`  
		Last Modified: Sat, 21 Oct 2023 02:15:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine`

```console
$ docker pull nats@sha256:7daf977fc2363f87a605d5d3d91ab29d618132dcd50b557077f5e58af1fac80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine` - linux; amd64

```console
$ docker pull nats@sha256:d4e4813552a56397c30eb67cc9954e4fe8d3c52f22044f8b58b89a74c1c2b4eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9273206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f427a6660eccfbbe3af8b73c44c617d299c54b23c990296e5e6294a71a43b77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 02:39:31 GMT
ENV NATS_SERVER=2.9.23
# Sat, 21 Oct 2023 02:39:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8c62d1c9f15651a22c4adaa9bfacffc3ade97f998bd5a5557074576ecf34bba2' ;; 		armhf) natsArch='arm6'; sha256='93c252b9ac70f22d6fbbc0bc8bc8624287dd0955a6c3bb5057e576af9c7d355a' ;; 		armv7) natsArch='arm7'; sha256='08e0c2a1b0d69135070464dce735038c99a882daadd1e3eaae050eacb61eac4c' ;; 		x86_64) natsArch='amd64'; sha256='8a52b6b4a0337d3c58ee70888bf605cc732d792d9babe6bc9c984a1967aff15f' ;; 		x86) natsArch='386'; sha256='102844ff97e19ab81728030e6a97e7cd7a228e63c07cc9132590d0193d3283d9' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 21 Oct 2023 02:39:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 21 Oct 2023 02:39:34 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 21 Oct 2023 02:39:34 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 02:39:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 02:39:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c12864ebc175352d54ebf3b232d82f3ab3bf6c9b1dba554a6c08befc5f1f5b0`  
		Last Modified: Sat, 21 Oct 2023 02:40:31 GMT  
		Size: 5.9 MB (5870241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf07cd39e612c04d3307720b94acd9ea5f045714c3c96b87c8664b60411f82ff`  
		Last Modified: Sat, 21 Oct 2023 02:40:30 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d395305b566fa3dc993d20653aef25fdd6cfb86a0907c9887730b3c1d033e87`  
		Last Modified: Sat, 21 Oct 2023 02:40:30 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:4bb591a46c9c180a21862ea80e57ac70fc729e275be026661f1fb8e0ead67fe1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8753029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34742494f5fc3fe733ebb1b6a46357cd873bdab366a5de6f5d7d6dc8575ee3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:29:21 GMT
ENV NATS_SERVER=2.9.23
# Sat, 21 Oct 2023 00:29:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8c62d1c9f15651a22c4adaa9bfacffc3ade97f998bd5a5557074576ecf34bba2' ;; 		armhf) natsArch='arm6'; sha256='93c252b9ac70f22d6fbbc0bc8bc8624287dd0955a6c3bb5057e576af9c7d355a' ;; 		armv7) natsArch='arm7'; sha256='08e0c2a1b0d69135070464dce735038c99a882daadd1e3eaae050eacb61eac4c' ;; 		x86_64) natsArch='amd64'; sha256='8a52b6b4a0337d3c58ee70888bf605cc732d792d9babe6bc9c984a1967aff15f' ;; 		x86) natsArch='386'; sha256='102844ff97e19ab81728030e6a97e7cd7a228e63c07cc9132590d0193d3283d9' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 21 Oct 2023 00:29:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 21 Oct 2023 00:29:23 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 21 Oct 2023 00:29:23 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 00:29:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 00:29:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d55b2ff64cab7abe39f10b4598a9c660c27f150c1bfab072ef67910f9f0b14d`  
		Last Modified: Sat, 21 Oct 2023 00:30:17 GMT  
		Size: 5.6 MB (5606735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3436a66e3650e606b9c204e6c9ae22b1deb22bcf85a713327f285fe4a0e9af`  
		Last Modified: Sat, 21 Oct 2023 00:30:16 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa9bc3aecaf5b6cb1b29fe2c0b0747db023c242a440a262f1d535cabdb456c4`  
		Last Modified: Sat, 21 Oct 2023 00:30:16 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:c953db98f59abc7266514b8aabce5165a5c828bb1758a35bbadcbb06bd6615ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8498719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff5af7882c169ad91990182482daf4ed92a8c423740f7807bda0dd3a662f1d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:53:13 GMT
ENV NATS_SERVER=2.9.23
# Sat, 21 Oct 2023 00:53:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8c62d1c9f15651a22c4adaa9bfacffc3ade97f998bd5a5557074576ecf34bba2' ;; 		armhf) natsArch='arm6'; sha256='93c252b9ac70f22d6fbbc0bc8bc8624287dd0955a6c3bb5057e576af9c7d355a' ;; 		armv7) natsArch='arm7'; sha256='08e0c2a1b0d69135070464dce735038c99a882daadd1e3eaae050eacb61eac4c' ;; 		x86_64) natsArch='amd64'; sha256='8a52b6b4a0337d3c58ee70888bf605cc732d792d9babe6bc9c984a1967aff15f' ;; 		x86) natsArch='386'; sha256='102844ff97e19ab81728030e6a97e7cd7a228e63c07cc9132590d0193d3283d9' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 21 Oct 2023 00:53:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 21 Oct 2023 00:53:16 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 21 Oct 2023 00:53:16 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 00:53:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 00:53:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8f14f7bf8a0570ca80faef91209b55fe068008a07cf597c10f0043ebeeeb59`  
		Last Modified: Sat, 21 Oct 2023 00:54:14 GMT  
		Size: 5.6 MB (5597816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9e48f1a2ad369454bcf0b3ad888d4e2e18c2fd2f9b1b8e0f3ca15adf0cb7fd`  
		Last Modified: Sat, 21 Oct 2023 00:54:13 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7cf48f507840bfca1fbeae4ed217a832402fa618cd118d7a05204b1a5291c2`  
		Last Modified: Sat, 21 Oct 2023 00:54:13 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1133e599549cadeefb1bcb1cac757f25af6ede5453695fe4fcf11bb2fc10f9d5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8740995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d393e1b35d2f1b3811448f538a2e52dcfd78abd625c86bcb53d4a6589468ccdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 02:13:46 GMT
ENV NATS_SERVER=2.9.23
# Sat, 21 Oct 2023 02:13:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8c62d1c9f15651a22c4adaa9bfacffc3ade97f998bd5a5557074576ecf34bba2' ;; 		armhf) natsArch='arm6'; sha256='93c252b9ac70f22d6fbbc0bc8bc8624287dd0955a6c3bb5057e576af9c7d355a' ;; 		armv7) natsArch='arm7'; sha256='08e0c2a1b0d69135070464dce735038c99a882daadd1e3eaae050eacb61eac4c' ;; 		x86_64) natsArch='amd64'; sha256='8a52b6b4a0337d3c58ee70888bf605cc732d792d9babe6bc9c984a1967aff15f' ;; 		x86) natsArch='386'; sha256='102844ff97e19ab81728030e6a97e7cd7a228e63c07cc9132590d0193d3283d9' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 21 Oct 2023 02:13:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 21 Oct 2023 02:13:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 21 Oct 2023 02:13:48 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 02:13:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 02:13:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7a6c5496e9009da9fdb6c9a57125ecd5b57b47b1222ad3d7cde3c07a7d4f19`  
		Last Modified: Sat, 21 Oct 2023 02:14:54 GMT  
		Size: 5.4 MB (5408163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1928920894245093d2c1cb18df022385f3b5ac500a85e5a1ebbb5faedbcc4234`  
		Last Modified: Sat, 21 Oct 2023 02:14:53 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9fc11b45615231987039db0e7298219219c4eb46f02b1fda6988432d163954`  
		Last Modified: Sat, 21 Oct 2023 02:14:53 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine3.18`

```console
$ docker pull nats@sha256:7daf977fc2363f87a605d5d3d91ab29d618132dcd50b557077f5e58af1fac80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:d4e4813552a56397c30eb67cc9954e4fe8d3c52f22044f8b58b89a74c1c2b4eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9273206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f427a6660eccfbbe3af8b73c44c617d299c54b23c990296e5e6294a71a43b77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 02:39:31 GMT
ENV NATS_SERVER=2.9.23
# Sat, 21 Oct 2023 02:39:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8c62d1c9f15651a22c4adaa9bfacffc3ade97f998bd5a5557074576ecf34bba2' ;; 		armhf) natsArch='arm6'; sha256='93c252b9ac70f22d6fbbc0bc8bc8624287dd0955a6c3bb5057e576af9c7d355a' ;; 		armv7) natsArch='arm7'; sha256='08e0c2a1b0d69135070464dce735038c99a882daadd1e3eaae050eacb61eac4c' ;; 		x86_64) natsArch='amd64'; sha256='8a52b6b4a0337d3c58ee70888bf605cc732d792d9babe6bc9c984a1967aff15f' ;; 		x86) natsArch='386'; sha256='102844ff97e19ab81728030e6a97e7cd7a228e63c07cc9132590d0193d3283d9' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 21 Oct 2023 02:39:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 21 Oct 2023 02:39:34 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 21 Oct 2023 02:39:34 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 02:39:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 02:39:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c12864ebc175352d54ebf3b232d82f3ab3bf6c9b1dba554a6c08befc5f1f5b0`  
		Last Modified: Sat, 21 Oct 2023 02:40:31 GMT  
		Size: 5.9 MB (5870241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf07cd39e612c04d3307720b94acd9ea5f045714c3c96b87c8664b60411f82ff`  
		Last Modified: Sat, 21 Oct 2023 02:40:30 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d395305b566fa3dc993d20653aef25fdd6cfb86a0907c9887730b3c1d033e87`  
		Last Modified: Sat, 21 Oct 2023 02:40:30 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:4bb591a46c9c180a21862ea80e57ac70fc729e275be026661f1fb8e0ead67fe1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8753029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34742494f5fc3fe733ebb1b6a46357cd873bdab366a5de6f5d7d6dc8575ee3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:29:21 GMT
ENV NATS_SERVER=2.9.23
# Sat, 21 Oct 2023 00:29:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8c62d1c9f15651a22c4adaa9bfacffc3ade97f998bd5a5557074576ecf34bba2' ;; 		armhf) natsArch='arm6'; sha256='93c252b9ac70f22d6fbbc0bc8bc8624287dd0955a6c3bb5057e576af9c7d355a' ;; 		armv7) natsArch='arm7'; sha256='08e0c2a1b0d69135070464dce735038c99a882daadd1e3eaae050eacb61eac4c' ;; 		x86_64) natsArch='amd64'; sha256='8a52b6b4a0337d3c58ee70888bf605cc732d792d9babe6bc9c984a1967aff15f' ;; 		x86) natsArch='386'; sha256='102844ff97e19ab81728030e6a97e7cd7a228e63c07cc9132590d0193d3283d9' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 21 Oct 2023 00:29:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 21 Oct 2023 00:29:23 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 21 Oct 2023 00:29:23 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 00:29:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 00:29:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d55b2ff64cab7abe39f10b4598a9c660c27f150c1bfab072ef67910f9f0b14d`  
		Last Modified: Sat, 21 Oct 2023 00:30:17 GMT  
		Size: 5.6 MB (5606735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3436a66e3650e606b9c204e6c9ae22b1deb22bcf85a713327f285fe4a0e9af`  
		Last Modified: Sat, 21 Oct 2023 00:30:16 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa9bc3aecaf5b6cb1b29fe2c0b0747db023c242a440a262f1d535cabdb456c4`  
		Last Modified: Sat, 21 Oct 2023 00:30:16 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:c953db98f59abc7266514b8aabce5165a5c828bb1758a35bbadcbb06bd6615ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8498719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff5af7882c169ad91990182482daf4ed92a8c423740f7807bda0dd3a662f1d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:53:13 GMT
ENV NATS_SERVER=2.9.23
# Sat, 21 Oct 2023 00:53:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8c62d1c9f15651a22c4adaa9bfacffc3ade97f998bd5a5557074576ecf34bba2' ;; 		armhf) natsArch='arm6'; sha256='93c252b9ac70f22d6fbbc0bc8bc8624287dd0955a6c3bb5057e576af9c7d355a' ;; 		armv7) natsArch='arm7'; sha256='08e0c2a1b0d69135070464dce735038c99a882daadd1e3eaae050eacb61eac4c' ;; 		x86_64) natsArch='amd64'; sha256='8a52b6b4a0337d3c58ee70888bf605cc732d792d9babe6bc9c984a1967aff15f' ;; 		x86) natsArch='386'; sha256='102844ff97e19ab81728030e6a97e7cd7a228e63c07cc9132590d0193d3283d9' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 21 Oct 2023 00:53:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 21 Oct 2023 00:53:16 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 21 Oct 2023 00:53:16 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 00:53:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 00:53:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8f14f7bf8a0570ca80faef91209b55fe068008a07cf597c10f0043ebeeeb59`  
		Last Modified: Sat, 21 Oct 2023 00:54:14 GMT  
		Size: 5.6 MB (5597816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9e48f1a2ad369454bcf0b3ad888d4e2e18c2fd2f9b1b8e0f3ca15adf0cb7fd`  
		Last Modified: Sat, 21 Oct 2023 00:54:13 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7cf48f507840bfca1fbeae4ed217a832402fa618cd118d7a05204b1a5291c2`  
		Last Modified: Sat, 21 Oct 2023 00:54:13 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1133e599549cadeefb1bcb1cac757f25af6ede5453695fe4fcf11bb2fc10f9d5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8740995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d393e1b35d2f1b3811448f538a2e52dcfd78abd625c86bcb53d4a6589468ccdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 02:13:46 GMT
ENV NATS_SERVER=2.9.23
# Sat, 21 Oct 2023 02:13:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8c62d1c9f15651a22c4adaa9bfacffc3ade97f998bd5a5557074576ecf34bba2' ;; 		armhf) natsArch='arm6'; sha256='93c252b9ac70f22d6fbbc0bc8bc8624287dd0955a6c3bb5057e576af9c7d355a' ;; 		armv7) natsArch='arm7'; sha256='08e0c2a1b0d69135070464dce735038c99a882daadd1e3eaae050eacb61eac4c' ;; 		x86_64) natsArch='amd64'; sha256='8a52b6b4a0337d3c58ee70888bf605cc732d792d9babe6bc9c984a1967aff15f' ;; 		x86) natsArch='386'; sha256='102844ff97e19ab81728030e6a97e7cd7a228e63c07cc9132590d0193d3283d9' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 21 Oct 2023 02:13:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 21 Oct 2023 02:13:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 21 Oct 2023 02:13:48 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 02:13:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 02:13:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7a6c5496e9009da9fdb6c9a57125ecd5b57b47b1222ad3d7cde3c07a7d4f19`  
		Last Modified: Sat, 21 Oct 2023 02:14:54 GMT  
		Size: 5.4 MB (5408163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1928920894245093d2c1cb18df022385f3b5ac500a85e5a1ebbb5faedbcc4234`  
		Last Modified: Sat, 21 Oct 2023 02:14:53 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9fc11b45615231987039db0e7298219219c4eb46f02b1fda6988432d163954`  
		Last Modified: Sat, 21 Oct 2023 02:14:53 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-linux`

```console
$ docker pull nats@sha256:f6eba7c6befccb26620202fbe389fec5f159cd8ff08f6c716ad59f1cb6ce1d84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-linux` - linux; amd64

```console
$ docker pull nats@sha256:7d149a46fee148c37fa3b2bca97ac72ab1f96ed1793f8114cfecb40adc754119
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5247112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d7fa3037dc87b27de3f83d3dcb521067502705385f652d472d31fa037af822`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 02:39:39 GMT
COPY file:71487567f54b75938083a2680d411bd9e194b037c12b743a3c280c58abd7e82f in /nats-server 
# Sat, 21 Oct 2023 02:39:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 02:39:39 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 02:39:40 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 02:39:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5d153758a0dd20c137d358179ec27f8aca298056d0b26005f90208c882f0c7fa`  
		Last Modified: Fri, 13 Oct 2023 20:22:03 GMT  
		Size: 5.2 MB (5246604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e10c8d3bbc8928c41b93c6acf289f4b157e058ca08c00bee7222d13f60ce5b`  
		Last Modified: Sat, 21 Oct 2023 02:40:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:e80d5b10ed40caa3cae83ffa38af5ef4bb0c64e0a2174439dac89888d070cfc3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4983318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f65e0f853a25dd0c5e95c7b124ee834aafd668a27728562f5992e6bf60bce3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 00:29:27 GMT
COPY file:a99ff6735b1292770195e5dfe0e7f8a56bae939bfb272c8cbdfb47e7ba6c4828 in /nats-server 
# Sat, 21 Oct 2023 00:29:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 00:29:27 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 00:29:27 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 00:29:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:217c24d6cc08c267f56e5da2ce4e101011c47ccc55a86d28c979a19ebcb92d1e`  
		Last Modified: Fri, 13 Oct 2023 20:50:41 GMT  
		Size: 5.0 MB (4982809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a18e8214bcecaf476164a2f5e27fbee68e657af02a45ccff4bec091d15044b`  
		Last Modified: Sat, 21 Oct 2023 00:30:30 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:02c1d43c056e7545dc87e85ec89da70f4a39471f78470e2297cb49fc28ab360e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4976291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b087a7c300c290914637afef3115233ccf803a2325dbe358b1340ca32dd1bb2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 00:53:29 GMT
COPY file:c45665aaa0d25bdd0098d10b44c0de8efea234c8bb8ca8d2159b85284914acec in /nats-server 
# Sat, 21 Oct 2023 00:53:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 00:53:30 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 00:53:30 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 00:53:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a4d0acc6fe81e822f8d7b966098f56b50e69fda2eaab5ba79292315f68bc3a00`  
		Last Modified: Fri, 13 Oct 2023 20:59:06 GMT  
		Size: 5.0 MB (4975782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54dd2e715bf93536d4168ea488cb9fded424844d693c284f42fa19b1b4e70c7c`  
		Last Modified: Sat, 21 Oct 2023 00:54:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f98ebc31879e3e27bb8297d98564bf27d043c6c282b963c110467d1072e6d9f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4784170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658fcb0e4f11ac4f89b118f5c21a1de8336d063fc32f8f08f638ea8345617886`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 02:14:05 GMT
COPY file:75276c307f8eba0e9701c41a06bc7811acfb74142d0dee0a37dfb289dfda3db1 in /nats-server 
# Sat, 21 Oct 2023 02:14:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 02:14:05 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 02:14:05 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 02:14:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c50a270bdf1d14f1505fe9a625df2c74a90941d423db84eb62da12b3b6c813a4`  
		Last Modified: Fri, 13 Oct 2023 20:42:09 GMT  
		Size: 4.8 MB (4783661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4996d72414c18f73392ed69b9132989e283146fe606df3028fe2096bd633de`  
		Last Modified: Sat, 21 Oct 2023 02:15:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver`

```console
$ docker pull nats@sha256:5f2553496dc3b061b01d6c71cc80555740c68717e704288786e7cdb2a58a5bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2.9-nanoserver` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:b12208fb5460efe7e1b62e0c46251c3a1daad5ee716d2705538fd4389c22386a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109797099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da2ca8c21a3ef708b1404687d739e38876f4ee7b5bdb23b6bcf873e39d9468ae`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 13 Oct 2023 20:21:13 GMT
RUN cmd /S /C #(nop) COPY file:00bfb4e63864da2c3a8640dc6372df1a1a5dae2d055af3e9d7902b58c0fcde95 in C:\nats-server.exe 
# Fri, 13 Oct 2023 20:21:14 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 13 Oct 2023 20:21:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 13 Oct 2023 20:21:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 13 Oct 2023 20:21:16 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db95068357ee7ae4d2b01d73f339f6beb88bcb4cc1c6d1fdbf47adaf4a83084`  
		Last Modified: Fri, 13 Oct 2023 20:22:45 GMT  
		Size: 5.3 MB (5326094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a669a99c0401b659048d6aefa3257d64d18e4e73d16f1a7f23c7ca16904bef23`  
		Last Modified: Fri, 13 Oct 2023 20:22:43 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ceeae736fe5ff6bea48a378d2dee9b4f5b515e62be43a6dbc5bf79f538744b`  
		Last Modified: Fri, 13 Oct 2023 20:22:43 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052d84a390e34e3943d4c689fdb1a58bde31d61ea65eb60ef264502597b9099a`  
		Last Modified: Fri, 13 Oct 2023 20:22:43 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14acdd2d288c743ff91da082ce23136b8977cbf691b19ba5c9fdadb5724d4e4b`  
		Last Modified: Fri, 13 Oct 2023 20:22:43 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver-1809`

```console
$ docker pull nats@sha256:5f2553496dc3b061b01d6c71cc80555740c68717e704288786e7cdb2a58a5bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2.9-nanoserver-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:b12208fb5460efe7e1b62e0c46251c3a1daad5ee716d2705538fd4389c22386a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109797099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da2ca8c21a3ef708b1404687d739e38876f4ee7b5bdb23b6bcf873e39d9468ae`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 13 Oct 2023 20:21:13 GMT
RUN cmd /S /C #(nop) COPY file:00bfb4e63864da2c3a8640dc6372df1a1a5dae2d055af3e9d7902b58c0fcde95 in C:\nats-server.exe 
# Fri, 13 Oct 2023 20:21:14 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 13 Oct 2023 20:21:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 13 Oct 2023 20:21:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 13 Oct 2023 20:21:16 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db95068357ee7ae4d2b01d73f339f6beb88bcb4cc1c6d1fdbf47adaf4a83084`  
		Last Modified: Fri, 13 Oct 2023 20:22:45 GMT  
		Size: 5.3 MB (5326094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a669a99c0401b659048d6aefa3257d64d18e4e73d16f1a7f23c7ca16904bef23`  
		Last Modified: Fri, 13 Oct 2023 20:22:43 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ceeae736fe5ff6bea48a378d2dee9b4f5b515e62be43a6dbc5bf79f538744b`  
		Last Modified: Fri, 13 Oct 2023 20:22:43 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052d84a390e34e3943d4c689fdb1a58bde31d61ea65eb60ef264502597b9099a`  
		Last Modified: Fri, 13 Oct 2023 20:22:43 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14acdd2d288c743ff91da082ce23136b8977cbf691b19ba5c9fdadb5724d4e4b`  
		Last Modified: Fri, 13 Oct 2023 20:22:43 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-scratch`

```console
$ docker pull nats@sha256:f6eba7c6befccb26620202fbe389fec5f159cd8ff08f6c716ad59f1cb6ce1d84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-scratch` - linux; amd64

```console
$ docker pull nats@sha256:7d149a46fee148c37fa3b2bca97ac72ab1f96ed1793f8114cfecb40adc754119
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5247112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d7fa3037dc87b27de3f83d3dcb521067502705385f652d472d31fa037af822`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 02:39:39 GMT
COPY file:71487567f54b75938083a2680d411bd9e194b037c12b743a3c280c58abd7e82f in /nats-server 
# Sat, 21 Oct 2023 02:39:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 02:39:39 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 02:39:40 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 02:39:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5d153758a0dd20c137d358179ec27f8aca298056d0b26005f90208c882f0c7fa`  
		Last Modified: Fri, 13 Oct 2023 20:22:03 GMT  
		Size: 5.2 MB (5246604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e10c8d3bbc8928c41b93c6acf289f4b157e058ca08c00bee7222d13f60ce5b`  
		Last Modified: Sat, 21 Oct 2023 02:40:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:e80d5b10ed40caa3cae83ffa38af5ef4bb0c64e0a2174439dac89888d070cfc3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4983318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f65e0f853a25dd0c5e95c7b124ee834aafd668a27728562f5992e6bf60bce3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 00:29:27 GMT
COPY file:a99ff6735b1292770195e5dfe0e7f8a56bae939bfb272c8cbdfb47e7ba6c4828 in /nats-server 
# Sat, 21 Oct 2023 00:29:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 00:29:27 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 00:29:27 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 00:29:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:217c24d6cc08c267f56e5da2ce4e101011c47ccc55a86d28c979a19ebcb92d1e`  
		Last Modified: Fri, 13 Oct 2023 20:50:41 GMT  
		Size: 5.0 MB (4982809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a18e8214bcecaf476164a2f5e27fbee68e657af02a45ccff4bec091d15044b`  
		Last Modified: Sat, 21 Oct 2023 00:30:30 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:02c1d43c056e7545dc87e85ec89da70f4a39471f78470e2297cb49fc28ab360e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4976291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b087a7c300c290914637afef3115233ccf803a2325dbe358b1340ca32dd1bb2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 00:53:29 GMT
COPY file:c45665aaa0d25bdd0098d10b44c0de8efea234c8bb8ca8d2159b85284914acec in /nats-server 
# Sat, 21 Oct 2023 00:53:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 00:53:30 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 00:53:30 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 00:53:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a4d0acc6fe81e822f8d7b966098f56b50e69fda2eaab5ba79292315f68bc3a00`  
		Last Modified: Fri, 13 Oct 2023 20:59:06 GMT  
		Size: 5.0 MB (4975782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54dd2e715bf93536d4168ea488cb9fded424844d693c284f42fa19b1b4e70c7c`  
		Last Modified: Sat, 21 Oct 2023 00:54:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f98ebc31879e3e27bb8297d98564bf27d043c6c282b963c110467d1072e6d9f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4784170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658fcb0e4f11ac4f89b118f5c21a1de8336d063fc32f8f08f638ea8345617886`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 02:14:05 GMT
COPY file:75276c307f8eba0e9701c41a06bc7811acfb74142d0dee0a37dfb289dfda3db1 in /nats-server 
# Sat, 21 Oct 2023 02:14:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 02:14:05 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 02:14:05 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 02:14:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c50a270bdf1d14f1505fe9a625df2c74a90941d423db84eb62da12b3b6c813a4`  
		Last Modified: Fri, 13 Oct 2023 20:42:09 GMT  
		Size: 4.8 MB (4783661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4996d72414c18f73392ed69b9132989e283146fe606df3028fe2096bd633de`  
		Last Modified: Sat, 21 Oct 2023 02:15:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore`

```console
$ docker pull nats@sha256:c7386cf07382c8b8bc8112303c10b0888d7183e75df844270bf95f3c6278d146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2.9-windowsservercore` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:d690406b91f8f4c855dc0dce4e5fc96b52394c84e1deb4db4ac3e3b76863e84d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2037672217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1896c6a11456cb73f29bb84dde01d5762f95793acbde0ca10557e869d13607af`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2023 03:32:17 GMT
ENV NATS_DOCKERIZED=1
# Fri, 13 Oct 2023 20:18:14 GMT
ENV NATS_SERVER=2.9.23
# Fri, 13 Oct 2023 20:18:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.23/nats-server-v2.9.23-windows-amd64.zip
# Fri, 13 Oct 2023 20:18:16 GMT
ENV NATS_SERVER_SHASUM=68604d0df9f276bf7773f67fd95267ee129662e7872e270707c852f056276db7
# Fri, 13 Oct 2023 20:19:16 GMT
RUN Set-PSDebug -Trace 2
# Fri, 13 Oct 2023 20:20:58 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 13 Oct 2023 20:20:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 13 Oct 2023 20:20:59 GMT
EXPOSE 4222 6222 8222
# Fri, 13 Oct 2023 20:21:00 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 13 Oct 2023 20:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4919cd870c32d33d8113b108e3e6ea2391bbbc70b2cf7e9febeeee307b1a4`  
		Last Modified: Wed, 11 Oct 2023 03:40:35 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce27dbaad0cf1a29b13da65c8ec2c9e6b42aaf192bb7138ab6c5b740dbd77b05`  
		Last Modified: Wed, 11 Oct 2023 03:40:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c067d6d13f4a842896f054d8faf94b4f19d2b893e661eb83255fef9f97427b51`  
		Last Modified: Fri, 13 Oct 2023 20:22:27 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed86b90b57ef0ff96cfb84a6b2299fafdcb441f4cdf20444bd6d8e08d30d1077`  
		Last Modified: Fri, 13 Oct 2023 20:22:27 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa67c6b32d2f520576f3cea8105a67acf43b87fb0b517485d0cafd2a93b83c1`  
		Last Modified: Fri, 13 Oct 2023 20:22:27 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6050ec1bea96c503aab3a151f6c042e3c749195a3122a52843aceaf051ea376`  
		Last Modified: Fri, 13 Oct 2023 20:22:27 GMT  
		Size: 449.8 KB (449761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87861da09dbd687e92f0b2fc6e3aeb110c75a58b1db499da489a19c0b555e34e`  
		Last Modified: Fri, 13 Oct 2023 20:22:26 GMT  
		Size: 5.6 MB (5618675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26716f4d0d22b10eea724fee02faa1237634263791c2a6dbc73faad09c93eebd`  
		Last Modified: Fri, 13 Oct 2023 20:22:25 GMT  
		Size: 1.9 KB (1941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b00496fe874c2269a71e1b085bbb727355b0d29893a6fe274a92cf3c482927`  
		Last Modified: Fri, 13 Oct 2023 20:22:25 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e3adaebf8fe75f24dcc73fe777e29cf10016f2516280fe6f7e64c2dc9d6a04`  
		Last Modified: Fri, 13 Oct 2023 20:22:25 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd0adb5e427986ffd48e87604a9b778cee3f62bd8c75f80840e00ccb4ffdead`  
		Last Modified: Fri, 13 Oct 2023 20:22:25 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore-1809`

```console
$ docker pull nats@sha256:c7386cf07382c8b8bc8112303c10b0888d7183e75df844270bf95f3c6278d146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2.9-windowsservercore-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:d690406b91f8f4c855dc0dce4e5fc96b52394c84e1deb4db4ac3e3b76863e84d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2037672217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1896c6a11456cb73f29bb84dde01d5762f95793acbde0ca10557e869d13607af`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2023 03:32:17 GMT
ENV NATS_DOCKERIZED=1
# Fri, 13 Oct 2023 20:18:14 GMT
ENV NATS_SERVER=2.9.23
# Fri, 13 Oct 2023 20:18:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.23/nats-server-v2.9.23-windows-amd64.zip
# Fri, 13 Oct 2023 20:18:16 GMT
ENV NATS_SERVER_SHASUM=68604d0df9f276bf7773f67fd95267ee129662e7872e270707c852f056276db7
# Fri, 13 Oct 2023 20:19:16 GMT
RUN Set-PSDebug -Trace 2
# Fri, 13 Oct 2023 20:20:58 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 13 Oct 2023 20:20:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 13 Oct 2023 20:20:59 GMT
EXPOSE 4222 6222 8222
# Fri, 13 Oct 2023 20:21:00 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 13 Oct 2023 20:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4919cd870c32d33d8113b108e3e6ea2391bbbc70b2cf7e9febeeee307b1a4`  
		Last Modified: Wed, 11 Oct 2023 03:40:35 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce27dbaad0cf1a29b13da65c8ec2c9e6b42aaf192bb7138ab6c5b740dbd77b05`  
		Last Modified: Wed, 11 Oct 2023 03:40:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c067d6d13f4a842896f054d8faf94b4f19d2b893e661eb83255fef9f97427b51`  
		Last Modified: Fri, 13 Oct 2023 20:22:27 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed86b90b57ef0ff96cfb84a6b2299fafdcb441f4cdf20444bd6d8e08d30d1077`  
		Last Modified: Fri, 13 Oct 2023 20:22:27 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa67c6b32d2f520576f3cea8105a67acf43b87fb0b517485d0cafd2a93b83c1`  
		Last Modified: Fri, 13 Oct 2023 20:22:27 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6050ec1bea96c503aab3a151f6c042e3c749195a3122a52843aceaf051ea376`  
		Last Modified: Fri, 13 Oct 2023 20:22:27 GMT  
		Size: 449.8 KB (449761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87861da09dbd687e92f0b2fc6e3aeb110c75a58b1db499da489a19c0b555e34e`  
		Last Modified: Fri, 13 Oct 2023 20:22:26 GMT  
		Size: 5.6 MB (5618675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26716f4d0d22b10eea724fee02faa1237634263791c2a6dbc73faad09c93eebd`  
		Last Modified: Fri, 13 Oct 2023 20:22:25 GMT  
		Size: 1.9 KB (1941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b00496fe874c2269a71e1b085bbb727355b0d29893a6fe274a92cf3c482927`  
		Last Modified: Fri, 13 Oct 2023 20:22:25 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e3adaebf8fe75f24dcc73fe777e29cf10016f2516280fe6f7e64c2dc9d6a04`  
		Last Modified: Fri, 13 Oct 2023 20:22:25 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd0adb5e427986ffd48e87604a9b778cee3f62bd8c75f80840e00ccb4ffdead`  
		Last Modified: Fri, 13 Oct 2023 20:22:25 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.23`

```console
$ docker pull nats@sha256:f6eba7c6befccb26620202fbe389fec5f159cd8ff08f6c716ad59f1cb6ce1d84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.23` - linux; amd64

```console
$ docker pull nats@sha256:7d149a46fee148c37fa3b2bca97ac72ab1f96ed1793f8114cfecb40adc754119
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5247112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d7fa3037dc87b27de3f83d3dcb521067502705385f652d472d31fa037af822`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 02:39:39 GMT
COPY file:71487567f54b75938083a2680d411bd9e194b037c12b743a3c280c58abd7e82f in /nats-server 
# Sat, 21 Oct 2023 02:39:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 02:39:39 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 02:39:40 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 02:39:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5d153758a0dd20c137d358179ec27f8aca298056d0b26005f90208c882f0c7fa`  
		Last Modified: Fri, 13 Oct 2023 20:22:03 GMT  
		Size: 5.2 MB (5246604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e10c8d3bbc8928c41b93c6acf289f4b157e058ca08c00bee7222d13f60ce5b`  
		Last Modified: Sat, 21 Oct 2023 02:40:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.23` - linux; arm variant v6

```console
$ docker pull nats@sha256:e80d5b10ed40caa3cae83ffa38af5ef4bb0c64e0a2174439dac89888d070cfc3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4983318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f65e0f853a25dd0c5e95c7b124ee834aafd668a27728562f5992e6bf60bce3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 00:29:27 GMT
COPY file:a99ff6735b1292770195e5dfe0e7f8a56bae939bfb272c8cbdfb47e7ba6c4828 in /nats-server 
# Sat, 21 Oct 2023 00:29:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 00:29:27 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 00:29:27 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 00:29:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:217c24d6cc08c267f56e5da2ce4e101011c47ccc55a86d28c979a19ebcb92d1e`  
		Last Modified: Fri, 13 Oct 2023 20:50:41 GMT  
		Size: 5.0 MB (4982809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a18e8214bcecaf476164a2f5e27fbee68e657af02a45ccff4bec091d15044b`  
		Last Modified: Sat, 21 Oct 2023 00:30:30 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.23` - linux; arm variant v7

```console
$ docker pull nats@sha256:02c1d43c056e7545dc87e85ec89da70f4a39471f78470e2297cb49fc28ab360e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4976291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b087a7c300c290914637afef3115233ccf803a2325dbe358b1340ca32dd1bb2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 00:53:29 GMT
COPY file:c45665aaa0d25bdd0098d10b44c0de8efea234c8bb8ca8d2159b85284914acec in /nats-server 
# Sat, 21 Oct 2023 00:53:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 00:53:30 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 00:53:30 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 00:53:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a4d0acc6fe81e822f8d7b966098f56b50e69fda2eaab5ba79292315f68bc3a00`  
		Last Modified: Fri, 13 Oct 2023 20:59:06 GMT  
		Size: 5.0 MB (4975782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54dd2e715bf93536d4168ea488cb9fded424844d693c284f42fa19b1b4e70c7c`  
		Last Modified: Sat, 21 Oct 2023 00:54:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.23` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f98ebc31879e3e27bb8297d98564bf27d043c6c282b963c110467d1072e6d9f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4784170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658fcb0e4f11ac4f89b118f5c21a1de8336d063fc32f8f08f638ea8345617886`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 02:14:05 GMT
COPY file:75276c307f8eba0e9701c41a06bc7811acfb74142d0dee0a37dfb289dfda3db1 in /nats-server 
# Sat, 21 Oct 2023 02:14:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 02:14:05 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 02:14:05 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 02:14:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c50a270bdf1d14f1505fe9a625df2c74a90941d423db84eb62da12b3b6c813a4`  
		Last Modified: Fri, 13 Oct 2023 20:42:09 GMT  
		Size: 4.8 MB (4783661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4996d72414c18f73392ed69b9132989e283146fe606df3028fe2096bd633de`  
		Last Modified: Sat, 21 Oct 2023 02:15:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.23-alpine`

```console
$ docker pull nats@sha256:7daf977fc2363f87a605d5d3d91ab29d618132dcd50b557077f5e58af1fac80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.23-alpine` - linux; amd64

```console
$ docker pull nats@sha256:d4e4813552a56397c30eb67cc9954e4fe8d3c52f22044f8b58b89a74c1c2b4eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9273206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f427a6660eccfbbe3af8b73c44c617d299c54b23c990296e5e6294a71a43b77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 02:39:31 GMT
ENV NATS_SERVER=2.9.23
# Sat, 21 Oct 2023 02:39:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8c62d1c9f15651a22c4adaa9bfacffc3ade97f998bd5a5557074576ecf34bba2' ;; 		armhf) natsArch='arm6'; sha256='93c252b9ac70f22d6fbbc0bc8bc8624287dd0955a6c3bb5057e576af9c7d355a' ;; 		armv7) natsArch='arm7'; sha256='08e0c2a1b0d69135070464dce735038c99a882daadd1e3eaae050eacb61eac4c' ;; 		x86_64) natsArch='amd64'; sha256='8a52b6b4a0337d3c58ee70888bf605cc732d792d9babe6bc9c984a1967aff15f' ;; 		x86) natsArch='386'; sha256='102844ff97e19ab81728030e6a97e7cd7a228e63c07cc9132590d0193d3283d9' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 21 Oct 2023 02:39:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 21 Oct 2023 02:39:34 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 21 Oct 2023 02:39:34 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 02:39:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 02:39:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c12864ebc175352d54ebf3b232d82f3ab3bf6c9b1dba554a6c08befc5f1f5b0`  
		Last Modified: Sat, 21 Oct 2023 02:40:31 GMT  
		Size: 5.9 MB (5870241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf07cd39e612c04d3307720b94acd9ea5f045714c3c96b87c8664b60411f82ff`  
		Last Modified: Sat, 21 Oct 2023 02:40:30 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d395305b566fa3dc993d20653aef25fdd6cfb86a0907c9887730b3c1d033e87`  
		Last Modified: Sat, 21 Oct 2023 02:40:30 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.23-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:4bb591a46c9c180a21862ea80e57ac70fc729e275be026661f1fb8e0ead67fe1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8753029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34742494f5fc3fe733ebb1b6a46357cd873bdab366a5de6f5d7d6dc8575ee3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:29:21 GMT
ENV NATS_SERVER=2.9.23
# Sat, 21 Oct 2023 00:29:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8c62d1c9f15651a22c4adaa9bfacffc3ade97f998bd5a5557074576ecf34bba2' ;; 		armhf) natsArch='arm6'; sha256='93c252b9ac70f22d6fbbc0bc8bc8624287dd0955a6c3bb5057e576af9c7d355a' ;; 		armv7) natsArch='arm7'; sha256='08e0c2a1b0d69135070464dce735038c99a882daadd1e3eaae050eacb61eac4c' ;; 		x86_64) natsArch='amd64'; sha256='8a52b6b4a0337d3c58ee70888bf605cc732d792d9babe6bc9c984a1967aff15f' ;; 		x86) natsArch='386'; sha256='102844ff97e19ab81728030e6a97e7cd7a228e63c07cc9132590d0193d3283d9' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 21 Oct 2023 00:29:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 21 Oct 2023 00:29:23 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 21 Oct 2023 00:29:23 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 00:29:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 00:29:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d55b2ff64cab7abe39f10b4598a9c660c27f150c1bfab072ef67910f9f0b14d`  
		Last Modified: Sat, 21 Oct 2023 00:30:17 GMT  
		Size: 5.6 MB (5606735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3436a66e3650e606b9c204e6c9ae22b1deb22bcf85a713327f285fe4a0e9af`  
		Last Modified: Sat, 21 Oct 2023 00:30:16 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa9bc3aecaf5b6cb1b29fe2c0b0747db023c242a440a262f1d535cabdb456c4`  
		Last Modified: Sat, 21 Oct 2023 00:30:16 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.23-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:c953db98f59abc7266514b8aabce5165a5c828bb1758a35bbadcbb06bd6615ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8498719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff5af7882c169ad91990182482daf4ed92a8c423740f7807bda0dd3a662f1d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:53:13 GMT
ENV NATS_SERVER=2.9.23
# Sat, 21 Oct 2023 00:53:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8c62d1c9f15651a22c4adaa9bfacffc3ade97f998bd5a5557074576ecf34bba2' ;; 		armhf) natsArch='arm6'; sha256='93c252b9ac70f22d6fbbc0bc8bc8624287dd0955a6c3bb5057e576af9c7d355a' ;; 		armv7) natsArch='arm7'; sha256='08e0c2a1b0d69135070464dce735038c99a882daadd1e3eaae050eacb61eac4c' ;; 		x86_64) natsArch='amd64'; sha256='8a52b6b4a0337d3c58ee70888bf605cc732d792d9babe6bc9c984a1967aff15f' ;; 		x86) natsArch='386'; sha256='102844ff97e19ab81728030e6a97e7cd7a228e63c07cc9132590d0193d3283d9' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 21 Oct 2023 00:53:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 21 Oct 2023 00:53:16 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 21 Oct 2023 00:53:16 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 00:53:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 00:53:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8f14f7bf8a0570ca80faef91209b55fe068008a07cf597c10f0043ebeeeb59`  
		Last Modified: Sat, 21 Oct 2023 00:54:14 GMT  
		Size: 5.6 MB (5597816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9e48f1a2ad369454bcf0b3ad888d4e2e18c2fd2f9b1b8e0f3ca15adf0cb7fd`  
		Last Modified: Sat, 21 Oct 2023 00:54:13 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7cf48f507840bfca1fbeae4ed217a832402fa618cd118d7a05204b1a5291c2`  
		Last Modified: Sat, 21 Oct 2023 00:54:13 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.23-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1133e599549cadeefb1bcb1cac757f25af6ede5453695fe4fcf11bb2fc10f9d5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8740995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d393e1b35d2f1b3811448f538a2e52dcfd78abd625c86bcb53d4a6589468ccdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 02:13:46 GMT
ENV NATS_SERVER=2.9.23
# Sat, 21 Oct 2023 02:13:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8c62d1c9f15651a22c4adaa9bfacffc3ade97f998bd5a5557074576ecf34bba2' ;; 		armhf) natsArch='arm6'; sha256='93c252b9ac70f22d6fbbc0bc8bc8624287dd0955a6c3bb5057e576af9c7d355a' ;; 		armv7) natsArch='arm7'; sha256='08e0c2a1b0d69135070464dce735038c99a882daadd1e3eaae050eacb61eac4c' ;; 		x86_64) natsArch='amd64'; sha256='8a52b6b4a0337d3c58ee70888bf605cc732d792d9babe6bc9c984a1967aff15f' ;; 		x86) natsArch='386'; sha256='102844ff97e19ab81728030e6a97e7cd7a228e63c07cc9132590d0193d3283d9' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 21 Oct 2023 02:13:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 21 Oct 2023 02:13:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 21 Oct 2023 02:13:48 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 02:13:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 02:13:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7a6c5496e9009da9fdb6c9a57125ecd5b57b47b1222ad3d7cde3c07a7d4f19`  
		Last Modified: Sat, 21 Oct 2023 02:14:54 GMT  
		Size: 5.4 MB (5408163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1928920894245093d2c1cb18df022385f3b5ac500a85e5a1ebbb5faedbcc4234`  
		Last Modified: Sat, 21 Oct 2023 02:14:53 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9fc11b45615231987039db0e7298219219c4eb46f02b1fda6988432d163954`  
		Last Modified: Sat, 21 Oct 2023 02:14:53 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.23-alpine3.18`

```console
$ docker pull nats@sha256:7daf977fc2363f87a605d5d3d91ab29d618132dcd50b557077f5e58af1fac80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.23-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:d4e4813552a56397c30eb67cc9954e4fe8d3c52f22044f8b58b89a74c1c2b4eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9273206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f427a6660eccfbbe3af8b73c44c617d299c54b23c990296e5e6294a71a43b77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 02:39:31 GMT
ENV NATS_SERVER=2.9.23
# Sat, 21 Oct 2023 02:39:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8c62d1c9f15651a22c4adaa9bfacffc3ade97f998bd5a5557074576ecf34bba2' ;; 		armhf) natsArch='arm6'; sha256='93c252b9ac70f22d6fbbc0bc8bc8624287dd0955a6c3bb5057e576af9c7d355a' ;; 		armv7) natsArch='arm7'; sha256='08e0c2a1b0d69135070464dce735038c99a882daadd1e3eaae050eacb61eac4c' ;; 		x86_64) natsArch='amd64'; sha256='8a52b6b4a0337d3c58ee70888bf605cc732d792d9babe6bc9c984a1967aff15f' ;; 		x86) natsArch='386'; sha256='102844ff97e19ab81728030e6a97e7cd7a228e63c07cc9132590d0193d3283d9' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 21 Oct 2023 02:39:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 21 Oct 2023 02:39:34 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 21 Oct 2023 02:39:34 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 02:39:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 02:39:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c12864ebc175352d54ebf3b232d82f3ab3bf6c9b1dba554a6c08befc5f1f5b0`  
		Last Modified: Sat, 21 Oct 2023 02:40:31 GMT  
		Size: 5.9 MB (5870241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf07cd39e612c04d3307720b94acd9ea5f045714c3c96b87c8664b60411f82ff`  
		Last Modified: Sat, 21 Oct 2023 02:40:30 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d395305b566fa3dc993d20653aef25fdd6cfb86a0907c9887730b3c1d033e87`  
		Last Modified: Sat, 21 Oct 2023 02:40:30 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.23-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:4bb591a46c9c180a21862ea80e57ac70fc729e275be026661f1fb8e0ead67fe1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8753029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34742494f5fc3fe733ebb1b6a46357cd873bdab366a5de6f5d7d6dc8575ee3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:29:21 GMT
ENV NATS_SERVER=2.9.23
# Sat, 21 Oct 2023 00:29:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8c62d1c9f15651a22c4adaa9bfacffc3ade97f998bd5a5557074576ecf34bba2' ;; 		armhf) natsArch='arm6'; sha256='93c252b9ac70f22d6fbbc0bc8bc8624287dd0955a6c3bb5057e576af9c7d355a' ;; 		armv7) natsArch='arm7'; sha256='08e0c2a1b0d69135070464dce735038c99a882daadd1e3eaae050eacb61eac4c' ;; 		x86_64) natsArch='amd64'; sha256='8a52b6b4a0337d3c58ee70888bf605cc732d792d9babe6bc9c984a1967aff15f' ;; 		x86) natsArch='386'; sha256='102844ff97e19ab81728030e6a97e7cd7a228e63c07cc9132590d0193d3283d9' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 21 Oct 2023 00:29:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 21 Oct 2023 00:29:23 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 21 Oct 2023 00:29:23 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 00:29:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 00:29:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d55b2ff64cab7abe39f10b4598a9c660c27f150c1bfab072ef67910f9f0b14d`  
		Last Modified: Sat, 21 Oct 2023 00:30:17 GMT  
		Size: 5.6 MB (5606735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3436a66e3650e606b9c204e6c9ae22b1deb22bcf85a713327f285fe4a0e9af`  
		Last Modified: Sat, 21 Oct 2023 00:30:16 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa9bc3aecaf5b6cb1b29fe2c0b0747db023c242a440a262f1d535cabdb456c4`  
		Last Modified: Sat, 21 Oct 2023 00:30:16 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.23-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:c953db98f59abc7266514b8aabce5165a5c828bb1758a35bbadcbb06bd6615ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8498719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff5af7882c169ad91990182482daf4ed92a8c423740f7807bda0dd3a662f1d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:53:13 GMT
ENV NATS_SERVER=2.9.23
# Sat, 21 Oct 2023 00:53:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8c62d1c9f15651a22c4adaa9bfacffc3ade97f998bd5a5557074576ecf34bba2' ;; 		armhf) natsArch='arm6'; sha256='93c252b9ac70f22d6fbbc0bc8bc8624287dd0955a6c3bb5057e576af9c7d355a' ;; 		armv7) natsArch='arm7'; sha256='08e0c2a1b0d69135070464dce735038c99a882daadd1e3eaae050eacb61eac4c' ;; 		x86_64) natsArch='amd64'; sha256='8a52b6b4a0337d3c58ee70888bf605cc732d792d9babe6bc9c984a1967aff15f' ;; 		x86) natsArch='386'; sha256='102844ff97e19ab81728030e6a97e7cd7a228e63c07cc9132590d0193d3283d9' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 21 Oct 2023 00:53:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 21 Oct 2023 00:53:16 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 21 Oct 2023 00:53:16 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 00:53:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 00:53:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8f14f7bf8a0570ca80faef91209b55fe068008a07cf597c10f0043ebeeeb59`  
		Last Modified: Sat, 21 Oct 2023 00:54:14 GMT  
		Size: 5.6 MB (5597816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9e48f1a2ad369454bcf0b3ad888d4e2e18c2fd2f9b1b8e0f3ca15adf0cb7fd`  
		Last Modified: Sat, 21 Oct 2023 00:54:13 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7cf48f507840bfca1fbeae4ed217a832402fa618cd118d7a05204b1a5291c2`  
		Last Modified: Sat, 21 Oct 2023 00:54:13 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.23-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1133e599549cadeefb1bcb1cac757f25af6ede5453695fe4fcf11bb2fc10f9d5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8740995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d393e1b35d2f1b3811448f538a2e52dcfd78abd625c86bcb53d4a6589468ccdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 02:13:46 GMT
ENV NATS_SERVER=2.9.23
# Sat, 21 Oct 2023 02:13:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8c62d1c9f15651a22c4adaa9bfacffc3ade97f998bd5a5557074576ecf34bba2' ;; 		armhf) natsArch='arm6'; sha256='93c252b9ac70f22d6fbbc0bc8bc8624287dd0955a6c3bb5057e576af9c7d355a' ;; 		armv7) natsArch='arm7'; sha256='08e0c2a1b0d69135070464dce735038c99a882daadd1e3eaae050eacb61eac4c' ;; 		x86_64) natsArch='amd64'; sha256='8a52b6b4a0337d3c58ee70888bf605cc732d792d9babe6bc9c984a1967aff15f' ;; 		x86) natsArch='386'; sha256='102844ff97e19ab81728030e6a97e7cd7a228e63c07cc9132590d0193d3283d9' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 21 Oct 2023 02:13:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 21 Oct 2023 02:13:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 21 Oct 2023 02:13:48 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 02:13:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 02:13:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7a6c5496e9009da9fdb6c9a57125ecd5b57b47b1222ad3d7cde3c07a7d4f19`  
		Last Modified: Sat, 21 Oct 2023 02:14:54 GMT  
		Size: 5.4 MB (5408163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1928920894245093d2c1cb18df022385f3b5ac500a85e5a1ebbb5faedbcc4234`  
		Last Modified: Sat, 21 Oct 2023 02:14:53 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9fc11b45615231987039db0e7298219219c4eb46f02b1fda6988432d163954`  
		Last Modified: Sat, 21 Oct 2023 02:14:53 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.23-linux`

```console
$ docker pull nats@sha256:f6eba7c6befccb26620202fbe389fec5f159cd8ff08f6c716ad59f1cb6ce1d84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.23-linux` - linux; amd64

```console
$ docker pull nats@sha256:7d149a46fee148c37fa3b2bca97ac72ab1f96ed1793f8114cfecb40adc754119
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5247112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d7fa3037dc87b27de3f83d3dcb521067502705385f652d472d31fa037af822`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 02:39:39 GMT
COPY file:71487567f54b75938083a2680d411bd9e194b037c12b743a3c280c58abd7e82f in /nats-server 
# Sat, 21 Oct 2023 02:39:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 02:39:39 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 02:39:40 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 02:39:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5d153758a0dd20c137d358179ec27f8aca298056d0b26005f90208c882f0c7fa`  
		Last Modified: Fri, 13 Oct 2023 20:22:03 GMT  
		Size: 5.2 MB (5246604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e10c8d3bbc8928c41b93c6acf289f4b157e058ca08c00bee7222d13f60ce5b`  
		Last Modified: Sat, 21 Oct 2023 02:40:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.23-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:e80d5b10ed40caa3cae83ffa38af5ef4bb0c64e0a2174439dac89888d070cfc3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4983318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f65e0f853a25dd0c5e95c7b124ee834aafd668a27728562f5992e6bf60bce3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 00:29:27 GMT
COPY file:a99ff6735b1292770195e5dfe0e7f8a56bae939bfb272c8cbdfb47e7ba6c4828 in /nats-server 
# Sat, 21 Oct 2023 00:29:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 00:29:27 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 00:29:27 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 00:29:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:217c24d6cc08c267f56e5da2ce4e101011c47ccc55a86d28c979a19ebcb92d1e`  
		Last Modified: Fri, 13 Oct 2023 20:50:41 GMT  
		Size: 5.0 MB (4982809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a18e8214bcecaf476164a2f5e27fbee68e657af02a45ccff4bec091d15044b`  
		Last Modified: Sat, 21 Oct 2023 00:30:30 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.23-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:02c1d43c056e7545dc87e85ec89da70f4a39471f78470e2297cb49fc28ab360e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4976291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b087a7c300c290914637afef3115233ccf803a2325dbe358b1340ca32dd1bb2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 00:53:29 GMT
COPY file:c45665aaa0d25bdd0098d10b44c0de8efea234c8bb8ca8d2159b85284914acec in /nats-server 
# Sat, 21 Oct 2023 00:53:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 00:53:30 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 00:53:30 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 00:53:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a4d0acc6fe81e822f8d7b966098f56b50e69fda2eaab5ba79292315f68bc3a00`  
		Last Modified: Fri, 13 Oct 2023 20:59:06 GMT  
		Size: 5.0 MB (4975782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54dd2e715bf93536d4168ea488cb9fded424844d693c284f42fa19b1b4e70c7c`  
		Last Modified: Sat, 21 Oct 2023 00:54:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.23-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f98ebc31879e3e27bb8297d98564bf27d043c6c282b963c110467d1072e6d9f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4784170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658fcb0e4f11ac4f89b118f5c21a1de8336d063fc32f8f08f638ea8345617886`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 02:14:05 GMT
COPY file:75276c307f8eba0e9701c41a06bc7811acfb74142d0dee0a37dfb289dfda3db1 in /nats-server 
# Sat, 21 Oct 2023 02:14:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 02:14:05 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 02:14:05 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 02:14:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c50a270bdf1d14f1505fe9a625df2c74a90941d423db84eb62da12b3b6c813a4`  
		Last Modified: Fri, 13 Oct 2023 20:42:09 GMT  
		Size: 4.8 MB (4783661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4996d72414c18f73392ed69b9132989e283146fe606df3028fe2096bd633de`  
		Last Modified: Sat, 21 Oct 2023 02:15:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.23-nanoserver`

```console
$ docker pull nats@sha256:5f2553496dc3b061b01d6c71cc80555740c68717e704288786e7cdb2a58a5bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2.9.23-nanoserver` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:b12208fb5460efe7e1b62e0c46251c3a1daad5ee716d2705538fd4389c22386a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109797099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da2ca8c21a3ef708b1404687d739e38876f4ee7b5bdb23b6bcf873e39d9468ae`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 13 Oct 2023 20:21:13 GMT
RUN cmd /S /C #(nop) COPY file:00bfb4e63864da2c3a8640dc6372df1a1a5dae2d055af3e9d7902b58c0fcde95 in C:\nats-server.exe 
# Fri, 13 Oct 2023 20:21:14 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 13 Oct 2023 20:21:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 13 Oct 2023 20:21:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 13 Oct 2023 20:21:16 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db95068357ee7ae4d2b01d73f339f6beb88bcb4cc1c6d1fdbf47adaf4a83084`  
		Last Modified: Fri, 13 Oct 2023 20:22:45 GMT  
		Size: 5.3 MB (5326094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a669a99c0401b659048d6aefa3257d64d18e4e73d16f1a7f23c7ca16904bef23`  
		Last Modified: Fri, 13 Oct 2023 20:22:43 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ceeae736fe5ff6bea48a378d2dee9b4f5b515e62be43a6dbc5bf79f538744b`  
		Last Modified: Fri, 13 Oct 2023 20:22:43 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052d84a390e34e3943d4c689fdb1a58bde31d61ea65eb60ef264502597b9099a`  
		Last Modified: Fri, 13 Oct 2023 20:22:43 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14acdd2d288c743ff91da082ce23136b8977cbf691b19ba5c9fdadb5724d4e4b`  
		Last Modified: Fri, 13 Oct 2023 20:22:43 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.23-nanoserver-1809`

```console
$ docker pull nats@sha256:5f2553496dc3b061b01d6c71cc80555740c68717e704288786e7cdb2a58a5bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2.9.23-nanoserver-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:b12208fb5460efe7e1b62e0c46251c3a1daad5ee716d2705538fd4389c22386a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109797099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da2ca8c21a3ef708b1404687d739e38876f4ee7b5bdb23b6bcf873e39d9468ae`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 13 Oct 2023 20:21:13 GMT
RUN cmd /S /C #(nop) COPY file:00bfb4e63864da2c3a8640dc6372df1a1a5dae2d055af3e9d7902b58c0fcde95 in C:\nats-server.exe 
# Fri, 13 Oct 2023 20:21:14 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 13 Oct 2023 20:21:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 13 Oct 2023 20:21:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 13 Oct 2023 20:21:16 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db95068357ee7ae4d2b01d73f339f6beb88bcb4cc1c6d1fdbf47adaf4a83084`  
		Last Modified: Fri, 13 Oct 2023 20:22:45 GMT  
		Size: 5.3 MB (5326094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a669a99c0401b659048d6aefa3257d64d18e4e73d16f1a7f23c7ca16904bef23`  
		Last Modified: Fri, 13 Oct 2023 20:22:43 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ceeae736fe5ff6bea48a378d2dee9b4f5b515e62be43a6dbc5bf79f538744b`  
		Last Modified: Fri, 13 Oct 2023 20:22:43 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052d84a390e34e3943d4c689fdb1a58bde31d61ea65eb60ef264502597b9099a`  
		Last Modified: Fri, 13 Oct 2023 20:22:43 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14acdd2d288c743ff91da082ce23136b8977cbf691b19ba5c9fdadb5724d4e4b`  
		Last Modified: Fri, 13 Oct 2023 20:22:43 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.23-scratch`

```console
$ docker pull nats@sha256:f6eba7c6befccb26620202fbe389fec5f159cd8ff08f6c716ad59f1cb6ce1d84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.23-scratch` - linux; amd64

```console
$ docker pull nats@sha256:7d149a46fee148c37fa3b2bca97ac72ab1f96ed1793f8114cfecb40adc754119
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5247112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d7fa3037dc87b27de3f83d3dcb521067502705385f652d472d31fa037af822`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 02:39:39 GMT
COPY file:71487567f54b75938083a2680d411bd9e194b037c12b743a3c280c58abd7e82f in /nats-server 
# Sat, 21 Oct 2023 02:39:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 02:39:39 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 02:39:40 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 02:39:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5d153758a0dd20c137d358179ec27f8aca298056d0b26005f90208c882f0c7fa`  
		Last Modified: Fri, 13 Oct 2023 20:22:03 GMT  
		Size: 5.2 MB (5246604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e10c8d3bbc8928c41b93c6acf289f4b157e058ca08c00bee7222d13f60ce5b`  
		Last Modified: Sat, 21 Oct 2023 02:40:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.23-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:e80d5b10ed40caa3cae83ffa38af5ef4bb0c64e0a2174439dac89888d070cfc3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4983318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f65e0f853a25dd0c5e95c7b124ee834aafd668a27728562f5992e6bf60bce3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 00:29:27 GMT
COPY file:a99ff6735b1292770195e5dfe0e7f8a56bae939bfb272c8cbdfb47e7ba6c4828 in /nats-server 
# Sat, 21 Oct 2023 00:29:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 00:29:27 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 00:29:27 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 00:29:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:217c24d6cc08c267f56e5da2ce4e101011c47ccc55a86d28c979a19ebcb92d1e`  
		Last Modified: Fri, 13 Oct 2023 20:50:41 GMT  
		Size: 5.0 MB (4982809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a18e8214bcecaf476164a2f5e27fbee68e657af02a45ccff4bec091d15044b`  
		Last Modified: Sat, 21 Oct 2023 00:30:30 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.23-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:02c1d43c056e7545dc87e85ec89da70f4a39471f78470e2297cb49fc28ab360e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4976291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b087a7c300c290914637afef3115233ccf803a2325dbe358b1340ca32dd1bb2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 00:53:29 GMT
COPY file:c45665aaa0d25bdd0098d10b44c0de8efea234c8bb8ca8d2159b85284914acec in /nats-server 
# Sat, 21 Oct 2023 00:53:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 00:53:30 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 00:53:30 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 00:53:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a4d0acc6fe81e822f8d7b966098f56b50e69fda2eaab5ba79292315f68bc3a00`  
		Last Modified: Fri, 13 Oct 2023 20:59:06 GMT  
		Size: 5.0 MB (4975782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54dd2e715bf93536d4168ea488cb9fded424844d693c284f42fa19b1b4e70c7c`  
		Last Modified: Sat, 21 Oct 2023 00:54:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.23-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f98ebc31879e3e27bb8297d98564bf27d043c6c282b963c110467d1072e6d9f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4784170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658fcb0e4f11ac4f89b118f5c21a1de8336d063fc32f8f08f638ea8345617886`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 02:14:05 GMT
COPY file:75276c307f8eba0e9701c41a06bc7811acfb74142d0dee0a37dfb289dfda3db1 in /nats-server 
# Sat, 21 Oct 2023 02:14:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 02:14:05 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 02:14:05 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 02:14:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c50a270bdf1d14f1505fe9a625df2c74a90941d423db84eb62da12b3b6c813a4`  
		Last Modified: Fri, 13 Oct 2023 20:42:09 GMT  
		Size: 4.8 MB (4783661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4996d72414c18f73392ed69b9132989e283146fe606df3028fe2096bd633de`  
		Last Modified: Sat, 21 Oct 2023 02:15:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.23-windowsservercore`

```console
$ docker pull nats@sha256:c7386cf07382c8b8bc8112303c10b0888d7183e75df844270bf95f3c6278d146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2.9.23-windowsservercore` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:d690406b91f8f4c855dc0dce4e5fc96b52394c84e1deb4db4ac3e3b76863e84d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2037672217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1896c6a11456cb73f29bb84dde01d5762f95793acbde0ca10557e869d13607af`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2023 03:32:17 GMT
ENV NATS_DOCKERIZED=1
# Fri, 13 Oct 2023 20:18:14 GMT
ENV NATS_SERVER=2.9.23
# Fri, 13 Oct 2023 20:18:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.23/nats-server-v2.9.23-windows-amd64.zip
# Fri, 13 Oct 2023 20:18:16 GMT
ENV NATS_SERVER_SHASUM=68604d0df9f276bf7773f67fd95267ee129662e7872e270707c852f056276db7
# Fri, 13 Oct 2023 20:19:16 GMT
RUN Set-PSDebug -Trace 2
# Fri, 13 Oct 2023 20:20:58 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 13 Oct 2023 20:20:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 13 Oct 2023 20:20:59 GMT
EXPOSE 4222 6222 8222
# Fri, 13 Oct 2023 20:21:00 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 13 Oct 2023 20:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4919cd870c32d33d8113b108e3e6ea2391bbbc70b2cf7e9febeeee307b1a4`  
		Last Modified: Wed, 11 Oct 2023 03:40:35 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce27dbaad0cf1a29b13da65c8ec2c9e6b42aaf192bb7138ab6c5b740dbd77b05`  
		Last Modified: Wed, 11 Oct 2023 03:40:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c067d6d13f4a842896f054d8faf94b4f19d2b893e661eb83255fef9f97427b51`  
		Last Modified: Fri, 13 Oct 2023 20:22:27 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed86b90b57ef0ff96cfb84a6b2299fafdcb441f4cdf20444bd6d8e08d30d1077`  
		Last Modified: Fri, 13 Oct 2023 20:22:27 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa67c6b32d2f520576f3cea8105a67acf43b87fb0b517485d0cafd2a93b83c1`  
		Last Modified: Fri, 13 Oct 2023 20:22:27 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6050ec1bea96c503aab3a151f6c042e3c749195a3122a52843aceaf051ea376`  
		Last Modified: Fri, 13 Oct 2023 20:22:27 GMT  
		Size: 449.8 KB (449761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87861da09dbd687e92f0b2fc6e3aeb110c75a58b1db499da489a19c0b555e34e`  
		Last Modified: Fri, 13 Oct 2023 20:22:26 GMT  
		Size: 5.6 MB (5618675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26716f4d0d22b10eea724fee02faa1237634263791c2a6dbc73faad09c93eebd`  
		Last Modified: Fri, 13 Oct 2023 20:22:25 GMT  
		Size: 1.9 KB (1941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b00496fe874c2269a71e1b085bbb727355b0d29893a6fe274a92cf3c482927`  
		Last Modified: Fri, 13 Oct 2023 20:22:25 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e3adaebf8fe75f24dcc73fe777e29cf10016f2516280fe6f7e64c2dc9d6a04`  
		Last Modified: Fri, 13 Oct 2023 20:22:25 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd0adb5e427986ffd48e87604a9b778cee3f62bd8c75f80840e00ccb4ffdead`  
		Last Modified: Fri, 13 Oct 2023 20:22:25 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.23-windowsservercore-1809`

```console
$ docker pull nats@sha256:c7386cf07382c8b8bc8112303c10b0888d7183e75df844270bf95f3c6278d146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:2.9.23-windowsservercore-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:d690406b91f8f4c855dc0dce4e5fc96b52394c84e1deb4db4ac3e3b76863e84d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2037672217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1896c6a11456cb73f29bb84dde01d5762f95793acbde0ca10557e869d13607af`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2023 03:32:17 GMT
ENV NATS_DOCKERIZED=1
# Fri, 13 Oct 2023 20:18:14 GMT
ENV NATS_SERVER=2.9.23
# Fri, 13 Oct 2023 20:18:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.23/nats-server-v2.9.23-windows-amd64.zip
# Fri, 13 Oct 2023 20:18:16 GMT
ENV NATS_SERVER_SHASUM=68604d0df9f276bf7773f67fd95267ee129662e7872e270707c852f056276db7
# Fri, 13 Oct 2023 20:19:16 GMT
RUN Set-PSDebug -Trace 2
# Fri, 13 Oct 2023 20:20:58 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 13 Oct 2023 20:20:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 13 Oct 2023 20:20:59 GMT
EXPOSE 4222 6222 8222
# Fri, 13 Oct 2023 20:21:00 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 13 Oct 2023 20:21:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4919cd870c32d33d8113b108e3e6ea2391bbbc70b2cf7e9febeeee307b1a4`  
		Last Modified: Wed, 11 Oct 2023 03:40:35 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce27dbaad0cf1a29b13da65c8ec2c9e6b42aaf192bb7138ab6c5b740dbd77b05`  
		Last Modified: Wed, 11 Oct 2023 03:40:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c067d6d13f4a842896f054d8faf94b4f19d2b893e661eb83255fef9f97427b51`  
		Last Modified: Fri, 13 Oct 2023 20:22:27 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed86b90b57ef0ff96cfb84a6b2299fafdcb441f4cdf20444bd6d8e08d30d1077`  
		Last Modified: Fri, 13 Oct 2023 20:22:27 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa67c6b32d2f520576f3cea8105a67acf43b87fb0b517485d0cafd2a93b83c1`  
		Last Modified: Fri, 13 Oct 2023 20:22:27 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6050ec1bea96c503aab3a151f6c042e3c749195a3122a52843aceaf051ea376`  
		Last Modified: Fri, 13 Oct 2023 20:22:27 GMT  
		Size: 449.8 KB (449761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87861da09dbd687e92f0b2fc6e3aeb110c75a58b1db499da489a19c0b555e34e`  
		Last Modified: Fri, 13 Oct 2023 20:22:26 GMT  
		Size: 5.6 MB (5618675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26716f4d0d22b10eea724fee02faa1237634263791c2a6dbc73faad09c93eebd`  
		Last Modified: Fri, 13 Oct 2023 20:22:25 GMT  
		Size: 1.9 KB (1941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b00496fe874c2269a71e1b085bbb727355b0d29893a6fe274a92cf3c482927`  
		Last Modified: Fri, 13 Oct 2023 20:22:25 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e3adaebf8fe75f24dcc73fe777e29cf10016f2516280fe6f7e64c2dc9d6a04`  
		Last Modified: Fri, 13 Oct 2023 20:22:25 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd0adb5e427986ffd48e87604a9b778cee3f62bd8c75f80840e00ccb4ffdead`  
		Last Modified: Fri, 13 Oct 2023 20:22:25 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:d21d20ce210a5b2ad455f59fb1575e46408b8f3412915236fb9e5b42e2409bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:e3dc3554afb54f24b96cc8b9ed45304e3cdf4af3e0d825513842cccc6443f850
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9507519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861b77f7441d4a0fb6c985252a186dd754c2bbfffb97adef86dfd317af118334`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:24:10 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:24:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:24:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:24:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:24:12 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:24:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:24:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f36f68f29c67409263076c2054d9e936c2f5e1a55ee937eb688ec1ce4915b8f`  
		Last Modified: Fri, 27 Oct 2023 19:25:16 GMT  
		Size: 6.1 MB (6104549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3bd88fc72377412d689508327b2bddbd4b2809fc079dfcead61801da1e9883c`  
		Last Modified: Fri, 27 Oct 2023 19:25:15 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29d0d1b8451bb92780ecfbc6b0f6488f2dbe6544277150975c6cfe9f22e12e3`  
		Last Modified: Fri, 27 Oct 2023 19:25:15 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:3f88f59fb120cd5be7f12dc9d2fb4b443ff7cd301e1bd95254dc57f4d2ce6561
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8970070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07efe60769658973f2765083517eda81ef09d5bb126a31af0295381865319ceb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:49:22 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:49:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:49:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:49:25 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:49:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a4fa6d23f1c5bfabc6eef228ba8baad859591a66d6499d64906f0f27f6d922`  
		Last Modified: Fri, 27 Oct 2023 19:50:04 GMT  
		Size: 5.8 MB (5823776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dfe6a1c19a37a61b685e720cd1156f95339fd4f9a4a425de2d8660166d9262e`  
		Last Modified: Fri, 27 Oct 2023 19:50:03 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3442d93fb16090b52375f2f415c787201447a8ade97b668a970f125f54a37e`  
		Last Modified: Fri, 27 Oct 2023 19:50:03 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:f38e6a15d5aee9730165a0a42dcaff9ecb306765613d8bab7eb1cfe51c7a306b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8714613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45868af98d7975ae09eecf8c1ad64a141d32fdb6a194bdf9afafffc05284c7c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:57:32 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:57:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:57:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:57:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:57:35 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:57:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:57:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44387fce322d8b03c5a038b2ba2a5e50919536ca64fd3fd32dddedce21340409`  
		Last Modified: Fri, 27 Oct 2023 19:58:22 GMT  
		Size: 5.8 MB (5813708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43c9b7450ee82499c6b877fa3b396205a7a4401978c9abd93e1b06200e9e5b0`  
		Last Modified: Fri, 27 Oct 2023 19:58:21 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59161e165420801f1ca6fba02cdfe0a8f3ba106b5443f1973c93063309ba83a`  
		Last Modified: Fri, 27 Oct 2023 19:58:21 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8b122cc94ebf709dd7ac8dbf611b3cbb93d995761f7a0cf90c9f1bfdc721db30
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9012372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1202aa9cd9cdcca825729430f679709284ca27900947697c866d1ced15ae5691`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:39:47 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:39:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:39:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:39:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:39:49 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:39:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:39:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b401e86e5d329ffd1a089932b1a9105a8375d0b413dc151add60434ed63162d1`  
		Last Modified: Fri, 27 Oct 2023 19:40:42 GMT  
		Size: 5.7 MB (5679544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939868b32dc69dc261c1c70fc9f1e9f3954f898d303b8d4a37e7178c8bf6c58b`  
		Last Modified: Fri, 27 Oct 2023 19:40:41 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b0ee4d1df33e3c8250ff7240533a3ea68875726979421fc6d9f705f0acf8d7`  
		Last Modified: Fri, 27 Oct 2023 19:40:41 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.18`

```console
$ docker pull nats@sha256:d21d20ce210a5b2ad455f59fb1575e46408b8f3412915236fb9e5b42e2409bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:e3dc3554afb54f24b96cc8b9ed45304e3cdf4af3e0d825513842cccc6443f850
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9507519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861b77f7441d4a0fb6c985252a186dd754c2bbfffb97adef86dfd317af118334`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:24:10 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:24:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:24:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:24:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:24:12 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:24:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:24:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f36f68f29c67409263076c2054d9e936c2f5e1a55ee937eb688ec1ce4915b8f`  
		Last Modified: Fri, 27 Oct 2023 19:25:16 GMT  
		Size: 6.1 MB (6104549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3bd88fc72377412d689508327b2bddbd4b2809fc079dfcead61801da1e9883c`  
		Last Modified: Fri, 27 Oct 2023 19:25:15 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29d0d1b8451bb92780ecfbc6b0f6488f2dbe6544277150975c6cfe9f22e12e3`  
		Last Modified: Fri, 27 Oct 2023 19:25:15 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:3f88f59fb120cd5be7f12dc9d2fb4b443ff7cd301e1bd95254dc57f4d2ce6561
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8970070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07efe60769658973f2765083517eda81ef09d5bb126a31af0295381865319ceb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:49:22 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:49:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:49:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:49:25 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:49:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a4fa6d23f1c5bfabc6eef228ba8baad859591a66d6499d64906f0f27f6d922`  
		Last Modified: Fri, 27 Oct 2023 19:50:04 GMT  
		Size: 5.8 MB (5823776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dfe6a1c19a37a61b685e720cd1156f95339fd4f9a4a425de2d8660166d9262e`  
		Last Modified: Fri, 27 Oct 2023 19:50:03 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3442d93fb16090b52375f2f415c787201447a8ade97b668a970f125f54a37e`  
		Last Modified: Fri, 27 Oct 2023 19:50:03 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:f38e6a15d5aee9730165a0a42dcaff9ecb306765613d8bab7eb1cfe51c7a306b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8714613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45868af98d7975ae09eecf8c1ad64a141d32fdb6a194bdf9afafffc05284c7c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:57:32 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:57:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:57:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:57:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:57:35 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:57:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:57:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44387fce322d8b03c5a038b2ba2a5e50919536ca64fd3fd32dddedce21340409`  
		Last Modified: Fri, 27 Oct 2023 19:58:22 GMT  
		Size: 5.8 MB (5813708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43c9b7450ee82499c6b877fa3b396205a7a4401978c9abd93e1b06200e9e5b0`  
		Last Modified: Fri, 27 Oct 2023 19:58:21 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59161e165420801f1ca6fba02cdfe0a8f3ba106b5443f1973c93063309ba83a`  
		Last Modified: Fri, 27 Oct 2023 19:58:21 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8b122cc94ebf709dd7ac8dbf611b3cbb93d995761f7a0cf90c9f1bfdc721db30
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9012372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1202aa9cd9cdcca825729430f679709284ca27900947697c866d1ced15ae5691`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:39:47 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:39:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:39:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:39:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:39:49 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:39:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:39:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b401e86e5d329ffd1a089932b1a9105a8375d0b413dc151add60434ed63162d1`  
		Last Modified: Fri, 27 Oct 2023 19:40:42 GMT  
		Size: 5.7 MB (5679544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939868b32dc69dc261c1c70fc9f1e9f3954f898d303b8d4a37e7178c8bf6c58b`  
		Last Modified: Fri, 27 Oct 2023 19:40:41 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b0ee4d1df33e3c8250ff7240533a3ea68875726979421fc6d9f705f0acf8d7`  
		Last Modified: Fri, 27 Oct 2023 19:40:41 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:ab462f647d9460c169dde8a382ec59675ed1f65bad4617dbc9f1f007bd5a709b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4974; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:fe0f6382b8b6b1820004268a1e539cabf394046302ddb9bd1fe14be1d5771fbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5481847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211d523019caad51116b188eb0cf75ce76becdb5aa40535a9f786d29130792f4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:24:45 GMT
COPY file:8488714a53ceca0afd69fdc135a2e59f81f3008e24d351a22438b39d8ab405fe in /nats-server 
# Fri, 27 Oct 2023 19:24:45 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:24:45 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:24:45 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:24:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:db9df0ffe6fe1654cbad22b0ee4be8b11d47faa0ee2c6f353915285f56329500`  
		Last Modified: Fri, 27 Oct 2023 19:25:41 GMT  
		Size: 5.5 MB (5481338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89fadd4ca8047bf736c814f88e92efa539731e382b4419dee4eee68edbe42fe`  
		Last Modified: Fri, 27 Oct 2023 19:25:40 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:7d149a46fee148c37fa3b2bca97ac72ab1f96ed1793f8114cfecb40adc754119
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5247112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d7fa3037dc87b27de3f83d3dcb521067502705385f652d472d31fa037af822`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 02:39:39 GMT
COPY file:71487567f54b75938083a2680d411bd9e194b037c12b743a3c280c58abd7e82f in /nats-server 
# Sat, 21 Oct 2023 02:39:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 02:39:39 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 02:39:40 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 02:39:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5d153758a0dd20c137d358179ec27f8aca298056d0b26005f90208c882f0c7fa`  
		Last Modified: Fri, 13 Oct 2023 20:22:03 GMT  
		Size: 5.2 MB (5246604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e10c8d3bbc8928c41b93c6acf289f4b157e058ca08c00bee7222d13f60ce5b`  
		Last Modified: Sat, 21 Oct 2023 02:40:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:b86c68503d84530fc3cb5ab2b6020dfe898e9e6d9b56965c14886b3cbdb07fd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5200382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7fef18696d3fe7987d9a9cbb167d045bcf97d5d2a1ac6fb76e73c65abde696`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:49:36 GMT
COPY file:0b4bcbfc47b21cd20c0f98a685ba4fbd4a6e7c8df6268e72fa48d2886a177781 in /nats-server 
# Fri, 27 Oct 2023 19:49:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:49:36 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:260eff5507dab2d5105a6c9ea84fc78fb51e66c5435f05572b8f8e7767cb103d`  
		Last Modified: Fri, 27 Oct 2023 19:50:29 GMT  
		Size: 5.2 MB (5199874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2e9e51baf6f1fddbeae98b8fed44bf52c3b147232cdea2f33fe5943fa9dc31`  
		Last Modified: Fri, 27 Oct 2023 19:50:28 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:e80d5b10ed40caa3cae83ffa38af5ef4bb0c64e0a2174439dac89888d070cfc3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4983318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f65e0f853a25dd0c5e95c7b124ee834aafd668a27728562f5992e6bf60bce3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 00:29:27 GMT
COPY file:a99ff6735b1292770195e5dfe0e7f8a56bae939bfb272c8cbdfb47e7ba6c4828 in /nats-server 
# Sat, 21 Oct 2023 00:29:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 00:29:27 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 00:29:27 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 00:29:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:217c24d6cc08c267f56e5da2ce4e101011c47ccc55a86d28c979a19ebcb92d1e`  
		Last Modified: Fri, 13 Oct 2023 20:50:41 GMT  
		Size: 5.0 MB (4982809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a18e8214bcecaf476164a2f5e27fbee68e657af02a45ccff4bec091d15044b`  
		Last Modified: Sat, 21 Oct 2023 00:30:30 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:9dce1c1ce729311280470aea6cb425a506188b2702ed1c75cda8e3f9ca2c36cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a859c2a13d0117b167ecf3c1130927b23abd6d788d55a2b26b35fd4d620be46`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:57:55 GMT
COPY file:5c489921e9dd684fb5e69dbf0d2c211653f6ca6b326f9f51a3f93f307aaf7808 in /nats-server 
# Fri, 27 Oct 2023 19:57:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:57:55 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:57:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:57:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e5204dbd51882e4867707ab178f23fd54d6c30e072917169c12a29fb29f2d900`  
		Last Modified: Fri, 27 Oct 2023 19:58:47 GMT  
		Size: 5.2 MB (5191456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc4cb991a069da2c550a4b4951d01811893ef1032980a277f673ca096b05c6b`  
		Last Modified: Fri, 27 Oct 2023 19:58:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:02c1d43c056e7545dc87e85ec89da70f4a39471f78470e2297cb49fc28ab360e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4976291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b087a7c300c290914637afef3115233ccf803a2325dbe358b1340ca32dd1bb2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 00:53:29 GMT
COPY file:c45665aaa0d25bdd0098d10b44c0de8efea234c8bb8ca8d2159b85284914acec in /nats-server 
# Sat, 21 Oct 2023 00:53:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 00:53:30 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 00:53:30 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 00:53:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a4d0acc6fe81e822f8d7b966098f56b50e69fda2eaab5ba79292315f68bc3a00`  
		Last Modified: Fri, 13 Oct 2023 20:59:06 GMT  
		Size: 5.0 MB (4975782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54dd2e715bf93536d4168ea488cb9fded424844d693c284f42fa19b1b4e70c7c`  
		Last Modified: Sat, 21 Oct 2023 00:54:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f547fa8c881d35fe2ec8d56a11fa32761085624a63e47624f20479a909f211a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5056051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c67a74cebb43fc4328a7683d38e1bcc0f30c2d603719c7e7f61c6c84353f53`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:40:19 GMT
COPY file:f0fa68e74def803c21b6f8269a3c75cd778bc42000a0681fcf1756130f3f8f0f in /nats-server 
# Fri, 27 Oct 2023 19:40:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:40:19 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:40:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:40:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ffe5996a38553f591ab54d703f3bbdb0cc32449b2ad8947b797aedbcfdb9ab7a`  
		Last Modified: Fri, 27 Oct 2023 19:41:06 GMT  
		Size: 5.1 MB (5055542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d3f38440ca89ef0ecab71a2f19751047fee6a0a5c7361057d77b22ef77bcc6`  
		Last Modified: Fri, 27 Oct 2023 19:41:05 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f98ebc31879e3e27bb8297d98564bf27d043c6c282b963c110467d1072e6d9f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4784170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658fcb0e4f11ac4f89b118f5c21a1de8336d063fc32f8f08f638ea8345617886`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 21 Oct 2023 02:14:05 GMT
COPY file:75276c307f8eba0e9701c41a06bc7811acfb74142d0dee0a37dfb289dfda3db1 in /nats-server 
# Sat, 21 Oct 2023 02:14:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 21 Oct 2023 02:14:05 GMT
EXPOSE 4222 6222 8222
# Sat, 21 Oct 2023 02:14:05 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 21 Oct 2023 02:14:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c50a270bdf1d14f1505fe9a625df2c74a90941d423db84eb62da12b3b6c813a4`  
		Last Modified: Fri, 13 Oct 2023 20:42:09 GMT  
		Size: 4.8 MB (4783661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4996d72414c18f73392ed69b9132989e283146fe606df3028fe2096bd633de`  
		Last Modified: Sat, 21 Oct 2023 02:15:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:29e2152405ed849d5c5589a35cf02b73576e88e08f0adf67040f458759dd892e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110065642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c710ddccc8cd69660a72c1525134e455f160899596c1a5f5155ce6f586ebdf7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 27 Oct 2023 20:17:42 GMT
RUN cmd /S /C #(nop) COPY file:18d2b201bedf44d6cf20990a5e1d83d3832eede6b2be4d6fa577c7cc28820bc5 in C:\nats-server.exe 
# Fri, 27 Oct 2023 20:17:43 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 Oct 2023 20:17:43 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 20:17:44 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 Oct 2023 20:17:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d2c4e1901a577a53d576303c5fb185d5d603a51a5963cce465f38722e9e7e3`  
		Last Modified: Fri, 27 Oct 2023 20:18:46 GMT  
		Size: 5.6 MB (5594656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:708131235a1cef76196cb5edbf912ebbc24020f96d3b0d168efe49cd88760665`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43906e90b84754a9e07f7b317810dec4106ba10d159dfe5bad8f536f9e8a376`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f4774c11b47cdb1c9434e6a07a055c33e201ece83051fd6bef2bcb38b955cb`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1c20f4d32a522c57acefece567048f4c290d4245799d7957e49dabe8bec88d`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:4b0b2c55b843e8c73693a839f88d8e403414c171b5b109e3debd04b6a953f76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:fe0f6382b8b6b1820004268a1e539cabf394046302ddb9bd1fe14be1d5771fbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5481847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211d523019caad51116b188eb0cf75ce76becdb5aa40535a9f786d29130792f4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:24:45 GMT
COPY file:8488714a53ceca0afd69fdc135a2e59f81f3008e24d351a22438b39d8ab405fe in /nats-server 
# Fri, 27 Oct 2023 19:24:45 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:24:45 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:24:45 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:24:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:db9df0ffe6fe1654cbad22b0ee4be8b11d47faa0ee2c6f353915285f56329500`  
		Last Modified: Fri, 27 Oct 2023 19:25:41 GMT  
		Size: 5.5 MB (5481338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89fadd4ca8047bf736c814f88e92efa539731e382b4419dee4eee68edbe42fe`  
		Last Modified: Fri, 27 Oct 2023 19:25:40 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:b86c68503d84530fc3cb5ab2b6020dfe898e9e6d9b56965c14886b3cbdb07fd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5200382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7fef18696d3fe7987d9a9cbb167d045bcf97d5d2a1ac6fb76e73c65abde696`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:49:36 GMT
COPY file:0b4bcbfc47b21cd20c0f98a685ba4fbd4a6e7c8df6268e72fa48d2886a177781 in /nats-server 
# Fri, 27 Oct 2023 19:49:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:49:36 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:260eff5507dab2d5105a6c9ea84fc78fb51e66c5435f05572b8f8e7767cb103d`  
		Last Modified: Fri, 27 Oct 2023 19:50:29 GMT  
		Size: 5.2 MB (5199874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2e9e51baf6f1fddbeae98b8fed44bf52c3b147232cdea2f33fe5943fa9dc31`  
		Last Modified: Fri, 27 Oct 2023 19:50:28 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:9dce1c1ce729311280470aea6cb425a506188b2702ed1c75cda8e3f9ca2c36cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a859c2a13d0117b167ecf3c1130927b23abd6d788d55a2b26b35fd4d620be46`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:57:55 GMT
COPY file:5c489921e9dd684fb5e69dbf0d2c211653f6ca6b326f9f51a3f93f307aaf7808 in /nats-server 
# Fri, 27 Oct 2023 19:57:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:57:55 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:57:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:57:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e5204dbd51882e4867707ab178f23fd54d6c30e072917169c12a29fb29f2d900`  
		Last Modified: Fri, 27 Oct 2023 19:58:47 GMT  
		Size: 5.2 MB (5191456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc4cb991a069da2c550a4b4951d01811893ef1032980a277f673ca096b05c6b`  
		Last Modified: Fri, 27 Oct 2023 19:58:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f547fa8c881d35fe2ec8d56a11fa32761085624a63e47624f20479a909f211a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5056051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c67a74cebb43fc4328a7683d38e1bcc0f30c2d603719c7e7f61c6c84353f53`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:40:19 GMT
COPY file:f0fa68e74def803c21b6f8269a3c75cd778bc42000a0681fcf1756130f3f8f0f in /nats-server 
# Fri, 27 Oct 2023 19:40:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:40:19 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:40:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:40:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ffe5996a38553f591ab54d703f3bbdb0cc32449b2ad8947b797aedbcfdb9ab7a`  
		Last Modified: Fri, 27 Oct 2023 19:41:06 GMT  
		Size: 5.1 MB (5055542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d3f38440ca89ef0ecab71a2f19751047fee6a0a5c7361057d77b22ef77bcc6`  
		Last Modified: Fri, 27 Oct 2023 19:41:05 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:2dfff9132418c9602296d363dad4e205e785752d73ddca9f4537f91cd4db57c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:nanoserver` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:29e2152405ed849d5c5589a35cf02b73576e88e08f0adf67040f458759dd892e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110065642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c710ddccc8cd69660a72c1525134e455f160899596c1a5f5155ce6f586ebdf7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 27 Oct 2023 20:17:42 GMT
RUN cmd /S /C #(nop) COPY file:18d2b201bedf44d6cf20990a5e1d83d3832eede6b2be4d6fa577c7cc28820bc5 in C:\nats-server.exe 
# Fri, 27 Oct 2023 20:17:43 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 Oct 2023 20:17:43 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 20:17:44 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 Oct 2023 20:17:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d2c4e1901a577a53d576303c5fb185d5d603a51a5963cce465f38722e9e7e3`  
		Last Modified: Fri, 27 Oct 2023 20:18:46 GMT  
		Size: 5.6 MB (5594656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:708131235a1cef76196cb5edbf912ebbc24020f96d3b0d168efe49cd88760665`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43906e90b84754a9e07f7b317810dec4106ba10d159dfe5bad8f536f9e8a376`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f4774c11b47cdb1c9434e6a07a055c33e201ece83051fd6bef2bcb38b955cb`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1c20f4d32a522c57acefece567048f4c290d4245799d7957e49dabe8bec88d`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:2dfff9132418c9602296d363dad4e205e785752d73ddca9f4537f91cd4db57c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:29e2152405ed849d5c5589a35cf02b73576e88e08f0adf67040f458759dd892e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110065642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c710ddccc8cd69660a72c1525134e455f160899596c1a5f5155ce6f586ebdf7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 27 Oct 2023 20:17:42 GMT
RUN cmd /S /C #(nop) COPY file:18d2b201bedf44d6cf20990a5e1d83d3832eede6b2be4d6fa577c7cc28820bc5 in C:\nats-server.exe 
# Fri, 27 Oct 2023 20:17:43 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 Oct 2023 20:17:43 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 20:17:44 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 Oct 2023 20:17:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d2c4e1901a577a53d576303c5fb185d5d603a51a5963cce465f38722e9e7e3`  
		Last Modified: Fri, 27 Oct 2023 20:18:46 GMT  
		Size: 5.6 MB (5594656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:708131235a1cef76196cb5edbf912ebbc24020f96d3b0d168efe49cd88760665`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43906e90b84754a9e07f7b317810dec4106ba10d159dfe5bad8f536f9e8a376`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f4774c11b47cdb1c9434e6a07a055c33e201ece83051fd6bef2bcb38b955cb`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1c20f4d32a522c57acefece567048f4c290d4245799d7957e49dabe8bec88d`  
		Last Modified: Fri, 27 Oct 2023 20:18:45 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:4b0b2c55b843e8c73693a839f88d8e403414c171b5b109e3debd04b6a953f76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:fe0f6382b8b6b1820004268a1e539cabf394046302ddb9bd1fe14be1d5771fbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5481847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211d523019caad51116b188eb0cf75ce76becdb5aa40535a9f786d29130792f4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:24:45 GMT
COPY file:8488714a53ceca0afd69fdc135a2e59f81f3008e24d351a22438b39d8ab405fe in /nats-server 
# Fri, 27 Oct 2023 19:24:45 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:24:45 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:24:45 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:24:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:db9df0ffe6fe1654cbad22b0ee4be8b11d47faa0ee2c6f353915285f56329500`  
		Last Modified: Fri, 27 Oct 2023 19:25:41 GMT  
		Size: 5.5 MB (5481338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89fadd4ca8047bf736c814f88e92efa539731e382b4419dee4eee68edbe42fe`  
		Last Modified: Fri, 27 Oct 2023 19:25:40 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:b86c68503d84530fc3cb5ab2b6020dfe898e9e6d9b56965c14886b3cbdb07fd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5200382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7fef18696d3fe7987d9a9cbb167d045bcf97d5d2a1ac6fb76e73c65abde696`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:49:36 GMT
COPY file:0b4bcbfc47b21cd20c0f98a685ba4fbd4a6e7c8df6268e72fa48d2886a177781 in /nats-server 
# Fri, 27 Oct 2023 19:49:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:49:36 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:260eff5507dab2d5105a6c9ea84fc78fb51e66c5435f05572b8f8e7767cb103d`  
		Last Modified: Fri, 27 Oct 2023 19:50:29 GMT  
		Size: 5.2 MB (5199874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2e9e51baf6f1fddbeae98b8fed44bf52c3b147232cdea2f33fe5943fa9dc31`  
		Last Modified: Fri, 27 Oct 2023 19:50:28 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:9dce1c1ce729311280470aea6cb425a506188b2702ed1c75cda8e3f9ca2c36cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a859c2a13d0117b167ecf3c1130927b23abd6d788d55a2b26b35fd4d620be46`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:57:55 GMT
COPY file:5c489921e9dd684fb5e69dbf0d2c211653f6ca6b326f9f51a3f93f307aaf7808 in /nats-server 
# Fri, 27 Oct 2023 19:57:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:57:55 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:57:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:57:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e5204dbd51882e4867707ab178f23fd54d6c30e072917169c12a29fb29f2d900`  
		Last Modified: Fri, 27 Oct 2023 19:58:47 GMT  
		Size: 5.2 MB (5191456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc4cb991a069da2c550a4b4951d01811893ef1032980a277f673ca096b05c6b`  
		Last Modified: Fri, 27 Oct 2023 19:58:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f547fa8c881d35fe2ec8d56a11fa32761085624a63e47624f20479a909f211a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5056051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c67a74cebb43fc4328a7683d38e1bcc0f30c2d603719c7e7f61c6c84353f53`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Oct 2023 19:40:19 GMT
COPY file:f0fa68e74def803c21b6f8269a3c75cd778bc42000a0681fcf1756130f3f8f0f in /nats-server 
# Fri, 27 Oct 2023 19:40:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Oct 2023 19:40:19 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:40:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Oct 2023 19:40:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ffe5996a38553f591ab54d703f3bbdb0cc32449b2ad8947b797aedbcfdb9ab7a`  
		Last Modified: Fri, 27 Oct 2023 19:41:06 GMT  
		Size: 5.1 MB (5055542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d3f38440ca89ef0ecab71a2f19751047fee6a0a5c7361057d77b22ef77bcc6`  
		Last Modified: Fri, 27 Oct 2023 19:41:05 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:77937863d60c0bd41b4552832c1e825585180192728ef72fada7e777025c53e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:windowsservercore` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:4c07209387666f05878e9e5ae7b2ea5feabc48d1bec9b29529609573281e8b50
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2037948217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e9cdf75f9dd9ef8362501dca3e4ac1ac1fec7a948dbcf54f9a3381ba48425c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2023 03:32:17 GMT
ENV NATS_DOCKERIZED=1
# Fri, 27 Oct 2023 20:14:59 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 20:15:00 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.4/nats-server-v2.10.4-windows-amd64.zip
# Fri, 27 Oct 2023 20:15:00 GMT
ENV NATS_SERVER_SHASUM=8792f3578b6ba3c8f3fc7763da1aea0525e92a02657017831a7d14dfd86e4959
# Fri, 27 Oct 2023 20:15:56 GMT
RUN Set-PSDebug -Trace 2
# Fri, 27 Oct 2023 20:17:27 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 27 Oct 2023 20:17:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 Oct 2023 20:17:29 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 20:17:29 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 Oct 2023 20:17:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4919cd870c32d33d8113b108e3e6ea2391bbbc70b2cf7e9febeeee307b1a4`  
		Last Modified: Wed, 11 Oct 2023 03:40:35 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce27dbaad0cf1a29b13da65c8ec2c9e6b42aaf192bb7138ab6c5b740dbd77b05`  
		Last Modified: Wed, 11 Oct 2023 03:40:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeff23ed3e0ed1d47af9f5ba3e920f499df7461b6b573b9b8890894a817d4e75`  
		Last Modified: Fri, 27 Oct 2023 20:18:29 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687bf833004525211ca17823f9860a90dd003c3b892c5a408cea77feb2b2f657`  
		Last Modified: Fri, 27 Oct 2023 20:18:28 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e1e0eed1c2383c5f276e9864bae63d81808a836d2b5ad5809045ece6333d9d`  
		Last Modified: Fri, 27 Oct 2023 20:18:28 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0118469c9fe0e2307ec1b83c4d3be497c92225567d7442b8b4b146f077d6d248`  
		Last Modified: Fri, 27 Oct 2023 20:18:28 GMT  
		Size: 453.6 KB (453628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc366f4d0a9c64080edab305111762c36c9aae61164c3d341fe9354b6d2dd24c`  
		Last Modified: Fri, 27 Oct 2023 20:18:27 GMT  
		Size: 5.9 MB (5890774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca441f0e90699b8ec845791d94a479a4394595caaa203b5c46465e97b66039bf`  
		Last Modified: Fri, 27 Oct 2023 20:18:25 GMT  
		Size: 2.0 KB (1983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf52f2d7db58c482fbb66a79029866157c5109ebaa1502f55449091e1c2b4587`  
		Last Modified: Fri, 27 Oct 2023 20:18:25 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04b7cb73a561c0325b062bfd254f914ed85d7d87a33532704a94bdb95cf318e`  
		Last Modified: Fri, 27 Oct 2023 20:18:26 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c201e4889ec729fccadc69fde51e2dcb98d0ef71408c9b998cb0f0cd5737ef74`  
		Last Modified: Fri, 27 Oct 2023 20:18:26 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:77937863d60c0bd41b4552832c1e825585180192728ef72fada7e777025c53e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:4c07209387666f05878e9e5ae7b2ea5feabc48d1bec9b29529609573281e8b50
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2037948217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e9cdf75f9dd9ef8362501dca3e4ac1ac1fec7a948dbcf54f9a3381ba48425c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2023 03:32:17 GMT
ENV NATS_DOCKERIZED=1
# Fri, 27 Oct 2023 20:14:59 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 20:15:00 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.4/nats-server-v2.10.4-windows-amd64.zip
# Fri, 27 Oct 2023 20:15:00 GMT
ENV NATS_SERVER_SHASUM=8792f3578b6ba3c8f3fc7763da1aea0525e92a02657017831a7d14dfd86e4959
# Fri, 27 Oct 2023 20:15:56 GMT
RUN Set-PSDebug -Trace 2
# Fri, 27 Oct 2023 20:17:27 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 27 Oct 2023 20:17:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 27 Oct 2023 20:17:29 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 20:17:29 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 Oct 2023 20:17:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4919cd870c32d33d8113b108e3e6ea2391bbbc70b2cf7e9febeeee307b1a4`  
		Last Modified: Wed, 11 Oct 2023 03:40:35 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce27dbaad0cf1a29b13da65c8ec2c9e6b42aaf192bb7138ab6c5b740dbd77b05`  
		Last Modified: Wed, 11 Oct 2023 03:40:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeff23ed3e0ed1d47af9f5ba3e920f499df7461b6b573b9b8890894a817d4e75`  
		Last Modified: Fri, 27 Oct 2023 20:18:29 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687bf833004525211ca17823f9860a90dd003c3b892c5a408cea77feb2b2f657`  
		Last Modified: Fri, 27 Oct 2023 20:18:28 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e1e0eed1c2383c5f276e9864bae63d81808a836d2b5ad5809045ece6333d9d`  
		Last Modified: Fri, 27 Oct 2023 20:18:28 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0118469c9fe0e2307ec1b83c4d3be497c92225567d7442b8b4b146f077d6d248`  
		Last Modified: Fri, 27 Oct 2023 20:18:28 GMT  
		Size: 453.6 KB (453628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc366f4d0a9c64080edab305111762c36c9aae61164c3d341fe9354b6d2dd24c`  
		Last Modified: Fri, 27 Oct 2023 20:18:27 GMT  
		Size: 5.9 MB (5890774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca441f0e90699b8ec845791d94a479a4394595caaa203b5c46465e97b66039bf`  
		Last Modified: Fri, 27 Oct 2023 20:18:25 GMT  
		Size: 2.0 KB (1983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf52f2d7db58c482fbb66a79029866157c5109ebaa1502f55449091e1c2b4587`  
		Last Modified: Fri, 27 Oct 2023 20:18:25 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04b7cb73a561c0325b062bfd254f914ed85d7d87a33532704a94bdb95cf318e`  
		Last Modified: Fri, 27 Oct 2023 20:18:26 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c201e4889ec729fccadc69fde51e2dcb98d0ef71408c9b998cb0f0cd5737ef74`  
		Last Modified: Fri, 27 Oct 2023 20:18:26 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
