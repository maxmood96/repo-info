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
