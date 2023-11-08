## `nats:latest`

```console
$ docker pull nats@sha256:20ae148f7af7b5bf1a222a136e797c69d5c48e30d09fd2d06af19d5f47d442fa
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
$ docker pull nats@sha256:ca5325d2a2c84eca8c4f3e3ba96a4fcf6dc91e97e3d3ebd3bae69f7a126c0e62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5248367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea934ed1a17a93225092fac66c8b617c594ecec00debda4eb753479eeadedab2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:22:58 GMT
COPY file:c3d82eee52a26292cc80755a2b88f8b80cef5c80fd438c99768cd1c33ca95a9d in /nats-server 
# Wed, 08 Nov 2023 19:22:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:22:59 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:22:59 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:22:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:44811b84801c95891b1ccde13fe7e76a1ffd8795cd2a066ac0630ee836c23c2e`  
		Last Modified: Wed, 08 Nov 2023 19:23:46 GMT  
		Size: 5.2 MB (5247859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8927d64e5da79549425963bee122f44117e41eaa442b01673188effd14c9b236`  
		Last Modified: Wed, 08 Nov 2023 19:23:46 GMT  
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
$ docker pull nats@sha256:4d3ccb1b790e4433d69872d7ddb8377aac40d6f000a66fa5b2795a62122a4f54
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4984842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f1a1ecd1b37c66268f966a88d26fa44b35f70909dedab19c60bfd5aca2035e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:49:29 GMT
COPY file:401de119a9fad5bd89c70f5a4d5c70f110d490ae5ab9aa60a7f963686ab297ee in /nats-server 
# Wed, 08 Nov 2023 19:49:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:49:29 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1d2c1b6f013f4386e7235452bc47cebd8001115c3a6504b418ee5b90071492a`  
		Last Modified: Wed, 08 Nov 2023 19:50:14 GMT  
		Size: 5.0 MB (4984334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5fea0f4bcfa87853f77179e249f0a8a09723aeb1c53882e3036fa6250a4ff5`  
		Last Modified: Wed, 08 Nov 2023 19:50:13 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:c73b24d4fb1ad910ad2f2bdefe0d18bfec11431afb4da9e3cd2be176e4fd49b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4977978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfe5b4a001ee28a1308edc00242441032b2afb69148c7ba17f692f75e2c1dba`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:57:47 GMT
COPY file:cd8c3bf2b10d14de1f76a0617be080153909dadcd658bb62cab16d41a650d3de in /nats-server 
# Wed, 08 Nov 2023 19:57:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:57:47 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:57:47 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:57:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e2a0a8d03803b71ab2e1e3540de965b9430b493bbd15bb2cb1372a7dd564c76d`  
		Last Modified: Wed, 08 Nov 2023 19:58:32 GMT  
		Size: 5.0 MB (4977470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfe9df0b73b8b228e9331792251ba43d36af5e4e898411b4f9b725bb8928231`  
		Last Modified: Wed, 08 Nov 2023 19:58:31 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:770e514bf6ca4d8b056bd9d16b7df5f56c45c587ce3c815515051b6588e38325
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4785043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75bc6347feea13831461567c92c52c13e9085417ef409fb74364cf63105e346`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:40:10 GMT
COPY file:209cf40c58f80a36d8d8c8060f48a598dcf03ae451d8d658f267d02f3ce7bddc in /nats-server 
# Wed, 08 Nov 2023 19:40:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:40:11 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:40:11 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:40:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b497fc8beff1c9fb319e3b4b62e22135e8e8d81506ede3ca51365887947a8571`  
		Last Modified: Wed, 08 Nov 2023 19:40:59 GMT  
		Size: 4.8 MB (4784535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cbc2e7980e0793ef96d07cc5a7d9418109519d7d6982ba49570b90d02b2932c`  
		Last Modified: Wed, 08 Nov 2023 19:40:59 GMT  
		Size: 508.0 B  
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
