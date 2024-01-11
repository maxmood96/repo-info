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
-	[`nats:2.10.8`](#nats2108)
-	[`nats:2.10.8-alpine`](#nats2108-alpine)
-	[`nats:2.10.8-alpine3.19`](#nats2108-alpine319)
-	[`nats:2.10.8-linux`](#nats2108-linux)
-	[`nats:2.10.8-nanoserver`](#nats2108-nanoserver)
-	[`nats:2.10.8-nanoserver-1809`](#nats2108-nanoserver-1809)
-	[`nats:2.10.8-scratch`](#nats2108-scratch)
-	[`nats:2.10.8-windowsservercore`](#nats2108-windowsservercore)
-	[`nats:2.10.8-windowsservercore-1809`](#nats2108-windowsservercore-1809)
-	[`nats:2.9`](#nats29)
-	[`nats:2.9-alpine`](#nats29-alpine)
-	[`nats:2.9-alpine3.18`](#nats29-alpine318)
-	[`nats:2.9-linux`](#nats29-linux)
-	[`nats:2.9-nanoserver`](#nats29-nanoserver)
-	[`nats:2.9-nanoserver-1809`](#nats29-nanoserver-1809)
-	[`nats:2.9-scratch`](#nats29-scratch)
-	[`nats:2.9-windowsservercore`](#nats29-windowsservercore)
-	[`nats:2.9-windowsservercore-1809`](#nats29-windowsservercore-1809)
-	[`nats:2.9.24`](#nats2924)
-	[`nats:2.9.24-alpine`](#nats2924-alpine)
-	[`nats:2.9.24-alpine3.18`](#nats2924-alpine318)
-	[`nats:2.9.24-linux`](#nats2924-linux)
-	[`nats:2.9.24-nanoserver`](#nats2924-nanoserver)
-	[`nats:2.9.24-nanoserver-1809`](#nats2924-nanoserver-1809)
-	[`nats:2.9.24-scratch`](#nats2924-scratch)
-	[`nats:2.9.24-windowsservercore`](#nats2924-windowsservercore)
-	[`nats:2.9.24-windowsservercore-1809`](#nats2924-windowsservercore-1809)
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
$ docker pull nats@sha256:bb9953704534e9f6a24a0345cfdda0f4c3c66cf7bcb04dd7dda86ffc16894ac1
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
	-	windows version 10.0.17763.5329; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:cfc16611986dc5883f4d27c9085e76910343d967594ee383d0255baeb057db79
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5501382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd357d7a18b1dda228ed5178c5ca385155fb364d30c57ca494ff97c8cd19309`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:48:54 GMT
COPY file:bfe22f1af895b2fc7a50837842688e659c05693b4bf069ba0376ffc69ae697ea in /nats-server 
# Thu, 11 Jan 2024 02:48:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:48:54 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:48:54 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:48:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7acebaf66611006473295971042ce1d190371c2a188cd83ac1294bdcbe941861`  
		Last Modified: Thu, 11 Jan 2024 02:49:55 GMT  
		Size: 5.5 MB (5500874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eaf929d718cd812eb25392358200a35e1e26347e9cfdce5e0b620aa8b735742`  
		Last Modified: Thu, 11 Jan 2024 02:49:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; amd64

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

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:25e7841f5b4c74faa1cefa3ac3a9b676cde24301bb4457381d45a631aeaed3af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0df98ee98ab731da5630054247a95f41befffd2873016036e7fe10c0f93ddb4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 07 Dec 2023 00:49:31 GMT
COPY file:57db66e8f632416070a8742db1e78e42b6a00178d3cafbb1d951f712bc1528b0 in /nats-server 
# Thu, 07 Dec 2023 00:49:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 07 Dec 2023 00:49:31 GMT
EXPOSE 4222 6222 8222
# Thu, 07 Dec 2023 00:49:31 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 07 Dec 2023 00:49:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dd9254a38d172bab9b5d4a85c3955a5bf8dc94569fdf541322f3006b8087cec0`  
		Last Modified: Thu, 07 Dec 2023 00:50:20 GMT  
		Size: 5.2 MB (5204791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30653da0be2fe0acec3ba9ba2b603cc6aa9511b5d611c70c10ecdd9b0709ad51`  
		Last Modified: Thu, 07 Dec 2023 00:50:19 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

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

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:a64d6b7675f0097a69544912df42b5d4e9b121bfff34649843637c53ab640cfb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5210866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3ae88cd2cd670d8b9b7f6e610fd3eb8687d499c38ca124f8033d847bbe8881`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:55:20 GMT
COPY file:8b6480435610d9164cd2c66bf75ef01eb81c3073e740cad17c74339e5baedda5 in /nats-server 
# Thu, 11 Jan 2024 02:55:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:55:21 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:55:21 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:55:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0920770a264f958a57c4e11d9c31cf4441041ea655047f6e857b67fad43906f9`  
		Last Modified: Thu, 11 Jan 2024 02:56:29 GMT  
		Size: 5.2 MB (5210357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c60b3bdf3047e4a3391384685743bd7f58305a89f5c71bd9b22fcd6e30211b`  
		Last Modified: Thu, 11 Jan 2024 02:56:28 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

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

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:187bdea269fa2454820b2e7d8e40ff4c70919e9caeac33af047e45e86f4e9118
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e480d5474031fbc4d95f443dc0e87b2d5bcfa6936887c9c20ddc78880966d3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:49:59 GMT
COPY file:8879823466eafef24f1fda27c9cd4f809446ce0288c6939e09932ffe25ab7b19 in /nats-server 
# Thu, 11 Jan 2024 02:50:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:50:00 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:50:00 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:50:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1e7857182cff537484895387bffc3495ec32bd159979fa4d1b851b83d7cd87c3`  
		Last Modified: Thu, 11 Jan 2024 02:50:57 GMT  
		Size: 5.1 MB (5075684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ac1735dae6ad6bb18f1075bbad502a9dc797d686f5c92486bd72aa9c38499e`  
		Last Modified: Thu, 11 Jan 2024 02:50:56 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

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

### `nats:2` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:ee000864a3122839be74300a01091298092421330414b26a5bd46dd177c45413
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110213906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3efb56477e7b9c48586d8290198510d573b31cedd83e0a3ffce9e7e6657e36`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 04:01:12 GMT
RUN cmd /S /C #(nop) COPY file:f6f49d606f9f811d8d95cfcbfc0c7db19c139753cf9d4aec8e19ceb60cae5eb7 in C:\nats-server.exe 
# Thu, 11 Jan 2024 04:01:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 04:01:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 04:01:14 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 04:01:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf42f1aafdb6016daeae38b38330cdd9dc19c174db9d4af6b68dd916e6eb084`  
		Last Modified: Thu, 11 Jan 2024 04:02:15 GMT  
		Size: 5.6 MB (5616337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c327a7a2c7b1f345092bbe2268b1cae828a27ee468658e4fd8894e7e6e66cc`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba577085c3d41035606a7eea09d46f81aa7b7d70cea80113a9f07d14e31ede2b`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506c8f4ceb3d31803fab29316067ffc5129a0d9b9c208f0b52fc86161329769a`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d929e177552db84f77ab4e31fc7399f97d242ff17d7b23874f7ef22d1c912e`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:35944c790dd59d33564fe85c8d5ae3085f2ffc0e38ee37254eeeb1a9cc5b9112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:ea36396a4460389cb144a9022eb5f3ea64591fb8a05f6d5d1a056db30fec8929
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6033b15096c9a633bd78cc2d815e6069d5b0f9f43e2d7208967ba46596f359d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 02:48:35 GMT
ENV NATS_SERVER=2.10.8
# Thu, 11 Jan 2024 02:48:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d74bba93d60a6a9836f4b54e942b8d4c2c9f33855659584cc7f76fdf8b1c4f7' ;; 		armhf) natsArch='arm6'; sha256='63147f419cda88e2d6f508e7a93dcc35803ad07d3a25bd5bdfdf3830f22a096d' ;; 		armv7) natsArch='arm7'; sha256='bc87934be36709f6f8928e5d65c7f11e8e2c5660826aa6c9af87b3a69cb6b8c3' ;; 		x86_64) natsArch='amd64'; sha256='23f647b813f339f0c8c2ac545f75bebcb2821dce0f47eca50e475e44b5d663d9' ;; 		x86) natsArch='386'; sha256='1ae8582969e34ff731bf065c724ad742ba2a1f566ad8de169b87f9e97b52f5ff' ;; 		s390x) natsArch='s390x'; sha256='826735b8333787b27191cf201162398b530f417f2b80f224fefcfa9d21b480c2' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:48:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:48:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:48:37 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:48:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:48:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f798ba46b67098bd15d5e60f4ba21bc7a74dea83bc32e096b2c4a69fcebd1c`  
		Last Modified: Thu, 11 Jan 2024 02:49:20 GMT  
		Size: 6.1 MB (6124277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa257ea47ccbcf0f4f7fc1790bf5eb92b3a0ae52e1ad2eeab796c971b4d8777`  
		Last Modified: Thu, 11 Jan 2024 02:49:19 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3196725eed73232f06492a1060fdba1af514ac24a95ee83078183e9cd6e93b7`  
		Last Modified: Thu, 11 Jan 2024 02:49:19 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:5646f5ce83a2cd0809dd62b9103aba3eff6bca2666965032ae01c1425f4c01c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8975747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17c0157045551d25e73637159044fae84067bde183e05d0099b9b806299b456`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Thu, 07 Dec 2023 00:49:19 GMT
ENV NATS_SERVER=2.10.7
# Thu, 07 Dec 2023 00:49:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='9a88afab7b3805475ff7250649447d8807dd52262011252e7faedec926d01782' ;; 		armhf) natsArch='arm6'; sha256='37f8d913cdc69143edf8bd20bceced053b90dba26d1fa94e2e07b6fe17f9db2e' ;; 		armv7) natsArch='arm7'; sha256='d96042f12ecc0578d193d5353c362a572384c6ad9a46db73b7cb5f28cb6e4ad2' ;; 		x86_64) natsArch='amd64'; sha256='91f5b493ce3151baa0b15d8bf093279dc94106dd56a201704a20de567607bcf7' ;; 		x86) natsArch='386'; sha256='a5cddcac9f8debaf45e7b9ba3960778b1c786020c690991094ce31d033ec7649' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 07 Dec 2023 00:49:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 07 Dec 2023 00:49:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 07 Dec 2023 00:49:22 GMT
EXPOSE 4222 6222 8222
# Thu, 07 Dec 2023 00:49:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Dec 2023 00:49:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733b743b5e93d5fde059f514131d51e22a1a4eef1fe4e71d4e42c7fdfc960da9`  
		Last Modified: Thu, 07 Dec 2023 00:49:56 GMT  
		Size: 5.8 MB (5827875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3b83a38bf1009764f2673fbcfe66e38ba7d57492c7838790e767319e64c961`  
		Last Modified: Thu, 07 Dec 2023 00:49:54 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b6d8395d698e101d9e4936dee08916549133753cd0672eceac8ddf1190193a`  
		Last Modified: Thu, 07 Dec 2023 00:49:54 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:f64cc78db496614d2464bc518395a9a9c18dcbced888bd246c53a5f607fb2798
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8753027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f43f54a537b58038fca151e541618e03368dcf372994c25b941d20ef6bb6dc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 02:54:55 GMT
ENV NATS_SERVER=2.10.8
# Thu, 11 Jan 2024 02:54:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d74bba93d60a6a9836f4b54e942b8d4c2c9f33855659584cc7f76fdf8b1c4f7' ;; 		armhf) natsArch='arm6'; sha256='63147f419cda88e2d6f508e7a93dcc35803ad07d3a25bd5bdfdf3830f22a096d' ;; 		armv7) natsArch='arm7'; sha256='bc87934be36709f6f8928e5d65c7f11e8e2c5660826aa6c9af87b3a69cb6b8c3' ;; 		x86_64) natsArch='amd64'; sha256='23f647b813f339f0c8c2ac545f75bebcb2821dce0f47eca50e475e44b5d663d9' ;; 		x86) natsArch='386'; sha256='1ae8582969e34ff731bf065c724ad742ba2a1f566ad8de169b87f9e97b52f5ff' ;; 		s390x) natsArch='s390x'; sha256='826735b8333787b27191cf201162398b530f417f2b80f224fefcfa9d21b480c2' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:54:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:54:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:55:00 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:55:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:55:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e8e103dfb44072b9bbf2eba7aad94fd639e561a22768da2bb37ea7d6729bab4`  
		Last Modified: Thu, 11 Jan 2024 02:55:51 GMT  
		Size: 5.8 MB (5833322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6faf32ab3656f6bddf90a09ced2d48b14b852842c566514822d55a40ed52361a`  
		Last Modified: Thu, 11 Jan 2024 02:55:50 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be21811ddbd891a760c2cc348a08f710ae14eeac84aa8d7d5af26c6581efc8e1`  
		Last Modified: Thu, 11 Jan 2024 02:55:49 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9244a34a1c67c86e4f309985a0c9ddc44c4a26dd32201cebc262d1a246f1e2d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9049174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4798f08bfc804e8b7077ab10105d2f686a6204a3f904209ec83f681962ea21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 02:49:45 GMT
ENV NATS_SERVER=2.10.8
# Thu, 11 Jan 2024 02:49:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d74bba93d60a6a9836f4b54e942b8d4c2c9f33855659584cc7f76fdf8b1c4f7' ;; 		armhf) natsArch='arm6'; sha256='63147f419cda88e2d6f508e7a93dcc35803ad07d3a25bd5bdfdf3830f22a096d' ;; 		armv7) natsArch='arm7'; sha256='bc87934be36709f6f8928e5d65c7f11e8e2c5660826aa6c9af87b3a69cb6b8c3' ;; 		x86_64) natsArch='amd64'; sha256='23f647b813f339f0c8c2ac545f75bebcb2821dce0f47eca50e475e44b5d663d9' ;; 		x86) natsArch='386'; sha256='1ae8582969e34ff731bf065c724ad742ba2a1f566ad8de169b87f9e97b52f5ff' ;; 		s390x) natsArch='s390x'; sha256='826735b8333787b27191cf201162398b530f417f2b80f224fefcfa9d21b480c2' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:49:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:49:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:49:48 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:49:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:49:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef2adfa7ed66cbcf98bfd19fd849cab6c342a8bf21efe1c363c1ec5d3c41ae0`  
		Last Modified: Thu, 11 Jan 2024 02:50:22 GMT  
		Size: 5.7 MB (5700378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c865cf9777bd8e4753ce89930261559591a9d2e030c0dbd995f82ba770e06f`  
		Last Modified: Thu, 11 Jan 2024 02:50:21 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1071663058684a0e820ec88c736711fda64c374c9a2492274176aadd0ef9bf83`  
		Last Modified: Thu, 11 Jan 2024 02:50:21 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.19`

```console
$ docker pull nats@sha256:1983fb960c52b05c1b212d459943fb024dac5419eda36bf55bf64279de68499d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.19` - linux; amd64

```console
$ docker pull nats@sha256:ea36396a4460389cb144a9022eb5f3ea64591fb8a05f6d5d1a056db30fec8929
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6033b15096c9a633bd78cc2d815e6069d5b0f9f43e2d7208967ba46596f359d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 02:48:35 GMT
ENV NATS_SERVER=2.10.8
# Thu, 11 Jan 2024 02:48:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d74bba93d60a6a9836f4b54e942b8d4c2c9f33855659584cc7f76fdf8b1c4f7' ;; 		armhf) natsArch='arm6'; sha256='63147f419cda88e2d6f508e7a93dcc35803ad07d3a25bd5bdfdf3830f22a096d' ;; 		armv7) natsArch='arm7'; sha256='bc87934be36709f6f8928e5d65c7f11e8e2c5660826aa6c9af87b3a69cb6b8c3' ;; 		x86_64) natsArch='amd64'; sha256='23f647b813f339f0c8c2ac545f75bebcb2821dce0f47eca50e475e44b5d663d9' ;; 		x86) natsArch='386'; sha256='1ae8582969e34ff731bf065c724ad742ba2a1f566ad8de169b87f9e97b52f5ff' ;; 		s390x) natsArch='s390x'; sha256='826735b8333787b27191cf201162398b530f417f2b80f224fefcfa9d21b480c2' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:48:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:48:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:48:37 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:48:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:48:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f798ba46b67098bd15d5e60f4ba21bc7a74dea83bc32e096b2c4a69fcebd1c`  
		Last Modified: Thu, 11 Jan 2024 02:49:20 GMT  
		Size: 6.1 MB (6124277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa257ea47ccbcf0f4f7fc1790bf5eb92b3a0ae52e1ad2eeab796c971b4d8777`  
		Last Modified: Thu, 11 Jan 2024 02:49:19 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3196725eed73232f06492a1060fdba1af514ac24a95ee83078183e9cd6e93b7`  
		Last Modified: Thu, 11 Jan 2024 02:49:19 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:f64cc78db496614d2464bc518395a9a9c18dcbced888bd246c53a5f607fb2798
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8753027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f43f54a537b58038fca151e541618e03368dcf372994c25b941d20ef6bb6dc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 02:54:55 GMT
ENV NATS_SERVER=2.10.8
# Thu, 11 Jan 2024 02:54:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d74bba93d60a6a9836f4b54e942b8d4c2c9f33855659584cc7f76fdf8b1c4f7' ;; 		armhf) natsArch='arm6'; sha256='63147f419cda88e2d6f508e7a93dcc35803ad07d3a25bd5bdfdf3830f22a096d' ;; 		armv7) natsArch='arm7'; sha256='bc87934be36709f6f8928e5d65c7f11e8e2c5660826aa6c9af87b3a69cb6b8c3' ;; 		x86_64) natsArch='amd64'; sha256='23f647b813f339f0c8c2ac545f75bebcb2821dce0f47eca50e475e44b5d663d9' ;; 		x86) natsArch='386'; sha256='1ae8582969e34ff731bf065c724ad742ba2a1f566ad8de169b87f9e97b52f5ff' ;; 		s390x) natsArch='s390x'; sha256='826735b8333787b27191cf201162398b530f417f2b80f224fefcfa9d21b480c2' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:54:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:54:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:55:00 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:55:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:55:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e8e103dfb44072b9bbf2eba7aad94fd639e561a22768da2bb37ea7d6729bab4`  
		Last Modified: Thu, 11 Jan 2024 02:55:51 GMT  
		Size: 5.8 MB (5833322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6faf32ab3656f6bddf90a09ced2d48b14b852842c566514822d55a40ed52361a`  
		Last Modified: Thu, 11 Jan 2024 02:55:50 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be21811ddbd891a760c2cc348a08f710ae14eeac84aa8d7d5af26c6581efc8e1`  
		Last Modified: Thu, 11 Jan 2024 02:55:49 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9244a34a1c67c86e4f309985a0c9ddc44c4a26dd32201cebc262d1a246f1e2d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9049174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4798f08bfc804e8b7077ab10105d2f686a6204a3f904209ec83f681962ea21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 02:49:45 GMT
ENV NATS_SERVER=2.10.8
# Thu, 11 Jan 2024 02:49:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d74bba93d60a6a9836f4b54e942b8d4c2c9f33855659584cc7f76fdf8b1c4f7' ;; 		armhf) natsArch='arm6'; sha256='63147f419cda88e2d6f508e7a93dcc35803ad07d3a25bd5bdfdf3830f22a096d' ;; 		armv7) natsArch='arm7'; sha256='bc87934be36709f6f8928e5d65c7f11e8e2c5660826aa6c9af87b3a69cb6b8c3' ;; 		x86_64) natsArch='amd64'; sha256='23f647b813f339f0c8c2ac545f75bebcb2821dce0f47eca50e475e44b5d663d9' ;; 		x86) natsArch='386'; sha256='1ae8582969e34ff731bf065c724ad742ba2a1f566ad8de169b87f9e97b52f5ff' ;; 		s390x) natsArch='s390x'; sha256='826735b8333787b27191cf201162398b530f417f2b80f224fefcfa9d21b480c2' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:49:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:49:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:49:48 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:49:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:49:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef2adfa7ed66cbcf98bfd19fd849cab6c342a8bf21efe1c363c1ec5d3c41ae0`  
		Last Modified: Thu, 11 Jan 2024 02:50:22 GMT  
		Size: 5.7 MB (5700378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c865cf9777bd8e4753ce89930261559591a9d2e030c0dbd995f82ba770e06f`  
		Last Modified: Thu, 11 Jan 2024 02:50:21 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1071663058684a0e820ec88c736711fda64c374c9a2492274176aadd0ef9bf83`  
		Last Modified: Thu, 11 Jan 2024 02:50:21 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:57e0b341099f0bd8156f8311f66e5c28cc1f9b0402b983d8dcaac59cf018ac60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:cfc16611986dc5883f4d27c9085e76910343d967594ee383d0255baeb057db79
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5501382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd357d7a18b1dda228ed5178c5ca385155fb364d30c57ca494ff97c8cd19309`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:48:54 GMT
COPY file:bfe22f1af895b2fc7a50837842688e659c05693b4bf069ba0376ffc69ae697ea in /nats-server 
# Thu, 11 Jan 2024 02:48:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:48:54 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:48:54 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:48:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7acebaf66611006473295971042ce1d190371c2a188cd83ac1294bdcbe941861`  
		Last Modified: Thu, 11 Jan 2024 02:49:55 GMT  
		Size: 5.5 MB (5500874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eaf929d718cd812eb25392358200a35e1e26347e9cfdce5e0b620aa8b735742`  
		Last Modified: Thu, 11 Jan 2024 02:49:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:25e7841f5b4c74faa1cefa3ac3a9b676cde24301bb4457381d45a631aeaed3af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0df98ee98ab731da5630054247a95f41befffd2873016036e7fe10c0f93ddb4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 07 Dec 2023 00:49:31 GMT
COPY file:57db66e8f632416070a8742db1e78e42b6a00178d3cafbb1d951f712bc1528b0 in /nats-server 
# Thu, 07 Dec 2023 00:49:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 07 Dec 2023 00:49:31 GMT
EXPOSE 4222 6222 8222
# Thu, 07 Dec 2023 00:49:31 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 07 Dec 2023 00:49:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dd9254a38d172bab9b5d4a85c3955a5bf8dc94569fdf541322f3006b8087cec0`  
		Last Modified: Thu, 07 Dec 2023 00:50:20 GMT  
		Size: 5.2 MB (5204791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30653da0be2fe0acec3ba9ba2b603cc6aa9511b5d611c70c10ecdd9b0709ad51`  
		Last Modified: Thu, 07 Dec 2023 00:50:19 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:a64d6b7675f0097a69544912df42b5d4e9b121bfff34649843637c53ab640cfb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5210866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3ae88cd2cd670d8b9b7f6e610fd3eb8687d499c38ca124f8033d847bbe8881`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:55:20 GMT
COPY file:8b6480435610d9164cd2c66bf75ef01eb81c3073e740cad17c74339e5baedda5 in /nats-server 
# Thu, 11 Jan 2024 02:55:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:55:21 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:55:21 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:55:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0920770a264f958a57c4e11d9c31cf4441041ea655047f6e857b67fad43906f9`  
		Last Modified: Thu, 11 Jan 2024 02:56:29 GMT  
		Size: 5.2 MB (5210357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c60b3bdf3047e4a3391384685743bd7f58305a89f5c71bd9b22fcd6e30211b`  
		Last Modified: Thu, 11 Jan 2024 02:56:28 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:187bdea269fa2454820b2e7d8e40ff4c70919e9caeac33af047e45e86f4e9118
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e480d5474031fbc4d95f443dc0e87b2d5bcfa6936887c9c20ddc78880966d3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:49:59 GMT
COPY file:8879823466eafef24f1fda27c9cd4f809446ce0288c6939e09932ffe25ab7b19 in /nats-server 
# Thu, 11 Jan 2024 02:50:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:50:00 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:50:00 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:50:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1e7857182cff537484895387bffc3495ec32bd159979fa4d1b851b83d7cd87c3`  
		Last Modified: Thu, 11 Jan 2024 02:50:57 GMT  
		Size: 5.1 MB (5075684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ac1735dae6ad6bb18f1075bbad502a9dc797d686f5c92486bd72aa9c38499e`  
		Last Modified: Thu, 11 Jan 2024 02:50:56 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:decd1f161f484155c8ca7a0c7e99247a35f4cb1b9d297b9f821b6e07246b56a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:ee000864a3122839be74300a01091298092421330414b26a5bd46dd177c45413
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110213906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3efb56477e7b9c48586d8290198510d573b31cedd83e0a3ffce9e7e6657e36`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 04:01:12 GMT
RUN cmd /S /C #(nop) COPY file:f6f49d606f9f811d8d95cfcbfc0c7db19c139753cf9d4aec8e19ceb60cae5eb7 in C:\nats-server.exe 
# Thu, 11 Jan 2024 04:01:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 04:01:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 04:01:14 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 04:01:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf42f1aafdb6016daeae38b38330cdd9dc19c174db9d4af6b68dd916e6eb084`  
		Last Modified: Thu, 11 Jan 2024 04:02:15 GMT  
		Size: 5.6 MB (5616337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c327a7a2c7b1f345092bbe2268b1cae828a27ee468658e4fd8894e7e6e66cc`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba577085c3d41035606a7eea09d46f81aa7b7d70cea80113a9f07d14e31ede2b`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506c8f4ceb3d31803fab29316067ffc5129a0d9b9c208f0b52fc86161329769a`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d929e177552db84f77ab4e31fc7399f97d242ff17d7b23874f7ef22d1c912e`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:decd1f161f484155c8ca7a0c7e99247a35f4cb1b9d297b9f821b6e07246b56a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:ee000864a3122839be74300a01091298092421330414b26a5bd46dd177c45413
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110213906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3efb56477e7b9c48586d8290198510d573b31cedd83e0a3ffce9e7e6657e36`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 04:01:12 GMT
RUN cmd /S /C #(nop) COPY file:f6f49d606f9f811d8d95cfcbfc0c7db19c139753cf9d4aec8e19ceb60cae5eb7 in C:\nats-server.exe 
# Thu, 11 Jan 2024 04:01:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 04:01:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 04:01:14 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 04:01:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf42f1aafdb6016daeae38b38330cdd9dc19c174db9d4af6b68dd916e6eb084`  
		Last Modified: Thu, 11 Jan 2024 04:02:15 GMT  
		Size: 5.6 MB (5616337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c327a7a2c7b1f345092bbe2268b1cae828a27ee468658e4fd8894e7e6e66cc`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba577085c3d41035606a7eea09d46f81aa7b7d70cea80113a9f07d14e31ede2b`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506c8f4ceb3d31803fab29316067ffc5129a0d9b9c208f0b52fc86161329769a`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d929e177552db84f77ab4e31fc7399f97d242ff17d7b23874f7ef22d1c912e`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:57e0b341099f0bd8156f8311f66e5c28cc1f9b0402b983d8dcaac59cf018ac60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:cfc16611986dc5883f4d27c9085e76910343d967594ee383d0255baeb057db79
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5501382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd357d7a18b1dda228ed5178c5ca385155fb364d30c57ca494ff97c8cd19309`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:48:54 GMT
COPY file:bfe22f1af895b2fc7a50837842688e659c05693b4bf069ba0376ffc69ae697ea in /nats-server 
# Thu, 11 Jan 2024 02:48:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:48:54 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:48:54 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:48:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7acebaf66611006473295971042ce1d190371c2a188cd83ac1294bdcbe941861`  
		Last Modified: Thu, 11 Jan 2024 02:49:55 GMT  
		Size: 5.5 MB (5500874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eaf929d718cd812eb25392358200a35e1e26347e9cfdce5e0b620aa8b735742`  
		Last Modified: Thu, 11 Jan 2024 02:49:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:25e7841f5b4c74faa1cefa3ac3a9b676cde24301bb4457381d45a631aeaed3af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0df98ee98ab731da5630054247a95f41befffd2873016036e7fe10c0f93ddb4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 07 Dec 2023 00:49:31 GMT
COPY file:57db66e8f632416070a8742db1e78e42b6a00178d3cafbb1d951f712bc1528b0 in /nats-server 
# Thu, 07 Dec 2023 00:49:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 07 Dec 2023 00:49:31 GMT
EXPOSE 4222 6222 8222
# Thu, 07 Dec 2023 00:49:31 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 07 Dec 2023 00:49:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dd9254a38d172bab9b5d4a85c3955a5bf8dc94569fdf541322f3006b8087cec0`  
		Last Modified: Thu, 07 Dec 2023 00:50:20 GMT  
		Size: 5.2 MB (5204791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30653da0be2fe0acec3ba9ba2b603cc6aa9511b5d611c70c10ecdd9b0709ad51`  
		Last Modified: Thu, 07 Dec 2023 00:50:19 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:a64d6b7675f0097a69544912df42b5d4e9b121bfff34649843637c53ab640cfb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5210866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3ae88cd2cd670d8b9b7f6e610fd3eb8687d499c38ca124f8033d847bbe8881`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:55:20 GMT
COPY file:8b6480435610d9164cd2c66bf75ef01eb81c3073e740cad17c74339e5baedda5 in /nats-server 
# Thu, 11 Jan 2024 02:55:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:55:21 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:55:21 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:55:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0920770a264f958a57c4e11d9c31cf4441041ea655047f6e857b67fad43906f9`  
		Last Modified: Thu, 11 Jan 2024 02:56:29 GMT  
		Size: 5.2 MB (5210357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c60b3bdf3047e4a3391384685743bd7f58305a89f5c71bd9b22fcd6e30211b`  
		Last Modified: Thu, 11 Jan 2024 02:56:28 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:187bdea269fa2454820b2e7d8e40ff4c70919e9caeac33af047e45e86f4e9118
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e480d5474031fbc4d95f443dc0e87b2d5bcfa6936887c9c20ddc78880966d3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:49:59 GMT
COPY file:8879823466eafef24f1fda27c9cd4f809446ce0288c6939e09932ffe25ab7b19 in /nats-server 
# Thu, 11 Jan 2024 02:50:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:50:00 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:50:00 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:50:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1e7857182cff537484895387bffc3495ec32bd159979fa4d1b851b83d7cd87c3`  
		Last Modified: Thu, 11 Jan 2024 02:50:57 GMT  
		Size: 5.1 MB (5075684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ac1735dae6ad6bb18f1075bbad502a9dc797d686f5c92486bd72aa9c38499e`  
		Last Modified: Thu, 11 Jan 2024 02:50:56 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:0bff0a4798c7f8bb2f02043d4d61e95f0c76717250d81c9e143d7ab3a2351a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:89f52b8b81a1fbf176205e5cb5caa71f8cc75b4fd9a057eda45eee9d007f0e6b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2076105215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99dc11e338875bec0e0c7c688468d40f6e3262afe6e4ab99858b86e9f2a2ba47`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 03:57:58 GMT
ENV NATS_SERVER=2.10.8
# Thu, 11 Jan 2024 03:57:59 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.8/nats-server-v2.10.8-windows-amd64.zip
# Thu, 11 Jan 2024 03:58:00 GMT
ENV NATS_SERVER_SHASUM=032ed7ebec9d3f40d9b096b005101a3568a2ab07bee93be9db089eef354f3dab
# Thu, 11 Jan 2024 03:59:12 GMT
RUN Set-PSDebug -Trace 2
# Thu, 11 Jan 2024 04:00:54 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 11 Jan 2024 04:00:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 04:00:55 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 04:00:56 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 04:00:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c6e78cb437ea2945136109e2881a48e24e24f66592ba7778be64331e4d2ccb`  
		Last Modified: Thu, 11 Jan 2024 04:01:58 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00914bffce2598259b34ebafa40823fc65864b8b43f937d9e3b7283d16e60f7`  
		Last Modified: Thu, 11 Jan 2024 04:01:58 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751940e3a482a7a84fd7a9741ca18de682fc19b1674c23c2d0d13872e842ed46`  
		Last Modified: Thu, 11 Jan 2024 04:01:58 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0123ebddfd37d224bec740e66f603c2345f82f4c08b38d32fac94721f733b6`  
		Last Modified: Thu, 11 Jan 2024 04:01:59 GMT  
		Size: 457.1 KB (457126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd190f787f1a3f9741dd6f585a98c58e1c0530276b617abccca895fed4e5dbc`  
		Last Modified: Thu, 11 Jan 2024 04:01:58 GMT  
		Size: 5.9 MB (5912649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f6de4df082e15ca15fd484cb3719198ab7ffb70c7e968ec7b20abc6185ad49`  
		Last Modified: Thu, 11 Jan 2024 04:01:56 GMT  
		Size: 1.9 KB (1941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b495bdea1d447e57b8bf347ca127dde4f38a0fbb092e876a032ac6ae3b7282`  
		Last Modified: Thu, 11 Jan 2024 04:01:56 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e041ce5ffd08bbec0256f9a994966ae544af0f4d2c49dc8ea7fff59e508865`  
		Last Modified: Thu, 11 Jan 2024 04:01:56 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d2322a5a4a23d0999899882871e27f86bbfbec89b82d95eac704cb6d02764d`  
		Last Modified: Thu, 11 Jan 2024 04:01:56 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:0bff0a4798c7f8bb2f02043d4d61e95f0c76717250d81c9e143d7ab3a2351a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:89f52b8b81a1fbf176205e5cb5caa71f8cc75b4fd9a057eda45eee9d007f0e6b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2076105215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99dc11e338875bec0e0c7c688468d40f6e3262afe6e4ab99858b86e9f2a2ba47`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 03:57:58 GMT
ENV NATS_SERVER=2.10.8
# Thu, 11 Jan 2024 03:57:59 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.8/nats-server-v2.10.8-windows-amd64.zip
# Thu, 11 Jan 2024 03:58:00 GMT
ENV NATS_SERVER_SHASUM=032ed7ebec9d3f40d9b096b005101a3568a2ab07bee93be9db089eef354f3dab
# Thu, 11 Jan 2024 03:59:12 GMT
RUN Set-PSDebug -Trace 2
# Thu, 11 Jan 2024 04:00:54 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 11 Jan 2024 04:00:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 04:00:55 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 04:00:56 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 04:00:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c6e78cb437ea2945136109e2881a48e24e24f66592ba7778be64331e4d2ccb`  
		Last Modified: Thu, 11 Jan 2024 04:01:58 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00914bffce2598259b34ebafa40823fc65864b8b43f937d9e3b7283d16e60f7`  
		Last Modified: Thu, 11 Jan 2024 04:01:58 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751940e3a482a7a84fd7a9741ca18de682fc19b1674c23c2d0d13872e842ed46`  
		Last Modified: Thu, 11 Jan 2024 04:01:58 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0123ebddfd37d224bec740e66f603c2345f82f4c08b38d32fac94721f733b6`  
		Last Modified: Thu, 11 Jan 2024 04:01:59 GMT  
		Size: 457.1 KB (457126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd190f787f1a3f9741dd6f585a98c58e1c0530276b617abccca895fed4e5dbc`  
		Last Modified: Thu, 11 Jan 2024 04:01:58 GMT  
		Size: 5.9 MB (5912649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f6de4df082e15ca15fd484cb3719198ab7ffb70c7e968ec7b20abc6185ad49`  
		Last Modified: Thu, 11 Jan 2024 04:01:56 GMT  
		Size: 1.9 KB (1941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b495bdea1d447e57b8bf347ca127dde4f38a0fbb092e876a032ac6ae3b7282`  
		Last Modified: Thu, 11 Jan 2024 04:01:56 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e041ce5ffd08bbec0256f9a994966ae544af0f4d2c49dc8ea7fff59e508865`  
		Last Modified: Thu, 11 Jan 2024 04:01:56 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d2322a5a4a23d0999899882871e27f86bbfbec89b82d95eac704cb6d02764d`  
		Last Modified: Thu, 11 Jan 2024 04:01:56 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:457087006c845025444ec5c81f4afe66932e086dffe9b6cccc804eb6204ddcc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.5329; amd64

### `nats:2.10` - linux; amd64

```console
$ docker pull nats@sha256:cfc16611986dc5883f4d27c9085e76910343d967594ee383d0255baeb057db79
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5501382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd357d7a18b1dda228ed5178c5ca385155fb364d30c57ca494ff97c8cd19309`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:48:54 GMT
COPY file:bfe22f1af895b2fc7a50837842688e659c05693b4bf069ba0376ffc69ae697ea in /nats-server 
# Thu, 11 Jan 2024 02:48:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:48:54 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:48:54 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:48:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7acebaf66611006473295971042ce1d190371c2a188cd83ac1294bdcbe941861`  
		Last Modified: Thu, 11 Jan 2024 02:49:55 GMT  
		Size: 5.5 MB (5500874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eaf929d718cd812eb25392358200a35e1e26347e9cfdce5e0b620aa8b735742`  
		Last Modified: Thu, 11 Jan 2024 02:49:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:25e7841f5b4c74faa1cefa3ac3a9b676cde24301bb4457381d45a631aeaed3af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0df98ee98ab731da5630054247a95f41befffd2873016036e7fe10c0f93ddb4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 07 Dec 2023 00:49:31 GMT
COPY file:57db66e8f632416070a8742db1e78e42b6a00178d3cafbb1d951f712bc1528b0 in /nats-server 
# Thu, 07 Dec 2023 00:49:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 07 Dec 2023 00:49:31 GMT
EXPOSE 4222 6222 8222
# Thu, 07 Dec 2023 00:49:31 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 07 Dec 2023 00:49:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dd9254a38d172bab9b5d4a85c3955a5bf8dc94569fdf541322f3006b8087cec0`  
		Last Modified: Thu, 07 Dec 2023 00:50:20 GMT  
		Size: 5.2 MB (5204791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30653da0be2fe0acec3ba9ba2b603cc6aa9511b5d611c70c10ecdd9b0709ad51`  
		Last Modified: Thu, 07 Dec 2023 00:50:19 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:a64d6b7675f0097a69544912df42b5d4e9b121bfff34649843637c53ab640cfb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5210866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3ae88cd2cd670d8b9b7f6e610fd3eb8687d499c38ca124f8033d847bbe8881`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:55:20 GMT
COPY file:8b6480435610d9164cd2c66bf75ef01eb81c3073e740cad17c74339e5baedda5 in /nats-server 
# Thu, 11 Jan 2024 02:55:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:55:21 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:55:21 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:55:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0920770a264f958a57c4e11d9c31cf4441041ea655047f6e857b67fad43906f9`  
		Last Modified: Thu, 11 Jan 2024 02:56:29 GMT  
		Size: 5.2 MB (5210357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c60b3bdf3047e4a3391384685743bd7f58305a89f5c71bd9b22fcd6e30211b`  
		Last Modified: Thu, 11 Jan 2024 02:56:28 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:187bdea269fa2454820b2e7d8e40ff4c70919e9caeac33af047e45e86f4e9118
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e480d5474031fbc4d95f443dc0e87b2d5bcfa6936887c9c20ddc78880966d3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:49:59 GMT
COPY file:8879823466eafef24f1fda27c9cd4f809446ce0288c6939e09932ffe25ab7b19 in /nats-server 
# Thu, 11 Jan 2024 02:50:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:50:00 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:50:00 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:50:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1e7857182cff537484895387bffc3495ec32bd159979fa4d1b851b83d7cd87c3`  
		Last Modified: Thu, 11 Jan 2024 02:50:57 GMT  
		Size: 5.1 MB (5075684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ac1735dae6ad6bb18f1075bbad502a9dc797d686f5c92486bd72aa9c38499e`  
		Last Modified: Thu, 11 Jan 2024 02:50:56 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:ee000864a3122839be74300a01091298092421330414b26a5bd46dd177c45413
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110213906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3efb56477e7b9c48586d8290198510d573b31cedd83e0a3ffce9e7e6657e36`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 04:01:12 GMT
RUN cmd /S /C #(nop) COPY file:f6f49d606f9f811d8d95cfcbfc0c7db19c139753cf9d4aec8e19ceb60cae5eb7 in C:\nats-server.exe 
# Thu, 11 Jan 2024 04:01:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 04:01:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 04:01:14 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 04:01:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf42f1aafdb6016daeae38b38330cdd9dc19c174db9d4af6b68dd916e6eb084`  
		Last Modified: Thu, 11 Jan 2024 04:02:15 GMT  
		Size: 5.6 MB (5616337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c327a7a2c7b1f345092bbe2268b1cae828a27ee468658e4fd8894e7e6e66cc`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba577085c3d41035606a7eea09d46f81aa7b7d70cea80113a9f07d14e31ede2b`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506c8f4ceb3d31803fab29316067ffc5129a0d9b9c208f0b52fc86161329769a`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d929e177552db84f77ab4e31fc7399f97d242ff17d7b23874f7ef22d1c912e`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:35944c790dd59d33564fe85c8d5ae3085f2ffc0e38ee37254eeeb1a9cc5b9112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10-alpine` - linux; amd64

```console
$ docker pull nats@sha256:ea36396a4460389cb144a9022eb5f3ea64591fb8a05f6d5d1a056db30fec8929
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6033b15096c9a633bd78cc2d815e6069d5b0f9f43e2d7208967ba46596f359d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 02:48:35 GMT
ENV NATS_SERVER=2.10.8
# Thu, 11 Jan 2024 02:48:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d74bba93d60a6a9836f4b54e942b8d4c2c9f33855659584cc7f76fdf8b1c4f7' ;; 		armhf) natsArch='arm6'; sha256='63147f419cda88e2d6f508e7a93dcc35803ad07d3a25bd5bdfdf3830f22a096d' ;; 		armv7) natsArch='arm7'; sha256='bc87934be36709f6f8928e5d65c7f11e8e2c5660826aa6c9af87b3a69cb6b8c3' ;; 		x86_64) natsArch='amd64'; sha256='23f647b813f339f0c8c2ac545f75bebcb2821dce0f47eca50e475e44b5d663d9' ;; 		x86) natsArch='386'; sha256='1ae8582969e34ff731bf065c724ad742ba2a1f566ad8de169b87f9e97b52f5ff' ;; 		s390x) natsArch='s390x'; sha256='826735b8333787b27191cf201162398b530f417f2b80f224fefcfa9d21b480c2' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:48:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:48:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:48:37 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:48:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:48:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f798ba46b67098bd15d5e60f4ba21bc7a74dea83bc32e096b2c4a69fcebd1c`  
		Last Modified: Thu, 11 Jan 2024 02:49:20 GMT  
		Size: 6.1 MB (6124277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa257ea47ccbcf0f4f7fc1790bf5eb92b3a0ae52e1ad2eeab796c971b4d8777`  
		Last Modified: Thu, 11 Jan 2024 02:49:19 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3196725eed73232f06492a1060fdba1af514ac24a95ee83078183e9cd6e93b7`  
		Last Modified: Thu, 11 Jan 2024 02:49:19 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:5646f5ce83a2cd0809dd62b9103aba3eff6bca2666965032ae01c1425f4c01c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8975747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17c0157045551d25e73637159044fae84067bde183e05d0099b9b806299b456`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Thu, 07 Dec 2023 00:49:19 GMT
ENV NATS_SERVER=2.10.7
# Thu, 07 Dec 2023 00:49:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='9a88afab7b3805475ff7250649447d8807dd52262011252e7faedec926d01782' ;; 		armhf) natsArch='arm6'; sha256='37f8d913cdc69143edf8bd20bceced053b90dba26d1fa94e2e07b6fe17f9db2e' ;; 		armv7) natsArch='arm7'; sha256='d96042f12ecc0578d193d5353c362a572384c6ad9a46db73b7cb5f28cb6e4ad2' ;; 		x86_64) natsArch='amd64'; sha256='91f5b493ce3151baa0b15d8bf093279dc94106dd56a201704a20de567607bcf7' ;; 		x86) natsArch='386'; sha256='a5cddcac9f8debaf45e7b9ba3960778b1c786020c690991094ce31d033ec7649' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 07 Dec 2023 00:49:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 07 Dec 2023 00:49:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 07 Dec 2023 00:49:22 GMT
EXPOSE 4222 6222 8222
# Thu, 07 Dec 2023 00:49:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Dec 2023 00:49:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733b743b5e93d5fde059f514131d51e22a1a4eef1fe4e71d4e42c7fdfc960da9`  
		Last Modified: Thu, 07 Dec 2023 00:49:56 GMT  
		Size: 5.8 MB (5827875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3b83a38bf1009764f2673fbcfe66e38ba7d57492c7838790e767319e64c961`  
		Last Modified: Thu, 07 Dec 2023 00:49:54 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b6d8395d698e101d9e4936dee08916549133753cd0672eceac8ddf1190193a`  
		Last Modified: Thu, 07 Dec 2023 00:49:54 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:f64cc78db496614d2464bc518395a9a9c18dcbced888bd246c53a5f607fb2798
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8753027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f43f54a537b58038fca151e541618e03368dcf372994c25b941d20ef6bb6dc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 02:54:55 GMT
ENV NATS_SERVER=2.10.8
# Thu, 11 Jan 2024 02:54:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d74bba93d60a6a9836f4b54e942b8d4c2c9f33855659584cc7f76fdf8b1c4f7' ;; 		armhf) natsArch='arm6'; sha256='63147f419cda88e2d6f508e7a93dcc35803ad07d3a25bd5bdfdf3830f22a096d' ;; 		armv7) natsArch='arm7'; sha256='bc87934be36709f6f8928e5d65c7f11e8e2c5660826aa6c9af87b3a69cb6b8c3' ;; 		x86_64) natsArch='amd64'; sha256='23f647b813f339f0c8c2ac545f75bebcb2821dce0f47eca50e475e44b5d663d9' ;; 		x86) natsArch='386'; sha256='1ae8582969e34ff731bf065c724ad742ba2a1f566ad8de169b87f9e97b52f5ff' ;; 		s390x) natsArch='s390x'; sha256='826735b8333787b27191cf201162398b530f417f2b80f224fefcfa9d21b480c2' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:54:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:54:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:55:00 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:55:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:55:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e8e103dfb44072b9bbf2eba7aad94fd639e561a22768da2bb37ea7d6729bab4`  
		Last Modified: Thu, 11 Jan 2024 02:55:51 GMT  
		Size: 5.8 MB (5833322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6faf32ab3656f6bddf90a09ced2d48b14b852842c566514822d55a40ed52361a`  
		Last Modified: Thu, 11 Jan 2024 02:55:50 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be21811ddbd891a760c2cc348a08f710ae14eeac84aa8d7d5af26c6581efc8e1`  
		Last Modified: Thu, 11 Jan 2024 02:55:49 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9244a34a1c67c86e4f309985a0c9ddc44c4a26dd32201cebc262d1a246f1e2d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9049174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4798f08bfc804e8b7077ab10105d2f686a6204a3f904209ec83f681962ea21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 02:49:45 GMT
ENV NATS_SERVER=2.10.8
# Thu, 11 Jan 2024 02:49:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d74bba93d60a6a9836f4b54e942b8d4c2c9f33855659584cc7f76fdf8b1c4f7' ;; 		armhf) natsArch='arm6'; sha256='63147f419cda88e2d6f508e7a93dcc35803ad07d3a25bd5bdfdf3830f22a096d' ;; 		armv7) natsArch='arm7'; sha256='bc87934be36709f6f8928e5d65c7f11e8e2c5660826aa6c9af87b3a69cb6b8c3' ;; 		x86_64) natsArch='amd64'; sha256='23f647b813f339f0c8c2ac545f75bebcb2821dce0f47eca50e475e44b5d663d9' ;; 		x86) natsArch='386'; sha256='1ae8582969e34ff731bf065c724ad742ba2a1f566ad8de169b87f9e97b52f5ff' ;; 		s390x) natsArch='s390x'; sha256='826735b8333787b27191cf201162398b530f417f2b80f224fefcfa9d21b480c2' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:49:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:49:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:49:48 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:49:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:49:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef2adfa7ed66cbcf98bfd19fd849cab6c342a8bf21efe1c363c1ec5d3c41ae0`  
		Last Modified: Thu, 11 Jan 2024 02:50:22 GMT  
		Size: 5.7 MB (5700378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c865cf9777bd8e4753ce89930261559591a9d2e030c0dbd995f82ba770e06f`  
		Last Modified: Thu, 11 Jan 2024 02:50:21 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1071663058684a0e820ec88c736711fda64c374c9a2492274176aadd0ef9bf83`  
		Last Modified: Thu, 11 Jan 2024 02:50:21 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine3.19`

```console
$ docker pull nats@sha256:1983fb960c52b05c1b212d459943fb024dac5419eda36bf55bf64279de68499d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10-alpine3.19` - linux; amd64

```console
$ docker pull nats@sha256:ea36396a4460389cb144a9022eb5f3ea64591fb8a05f6d5d1a056db30fec8929
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6033b15096c9a633bd78cc2d815e6069d5b0f9f43e2d7208967ba46596f359d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 02:48:35 GMT
ENV NATS_SERVER=2.10.8
# Thu, 11 Jan 2024 02:48:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d74bba93d60a6a9836f4b54e942b8d4c2c9f33855659584cc7f76fdf8b1c4f7' ;; 		armhf) natsArch='arm6'; sha256='63147f419cda88e2d6f508e7a93dcc35803ad07d3a25bd5bdfdf3830f22a096d' ;; 		armv7) natsArch='arm7'; sha256='bc87934be36709f6f8928e5d65c7f11e8e2c5660826aa6c9af87b3a69cb6b8c3' ;; 		x86_64) natsArch='amd64'; sha256='23f647b813f339f0c8c2ac545f75bebcb2821dce0f47eca50e475e44b5d663d9' ;; 		x86) natsArch='386'; sha256='1ae8582969e34ff731bf065c724ad742ba2a1f566ad8de169b87f9e97b52f5ff' ;; 		s390x) natsArch='s390x'; sha256='826735b8333787b27191cf201162398b530f417f2b80f224fefcfa9d21b480c2' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:48:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:48:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:48:37 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:48:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:48:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f798ba46b67098bd15d5e60f4ba21bc7a74dea83bc32e096b2c4a69fcebd1c`  
		Last Modified: Thu, 11 Jan 2024 02:49:20 GMT  
		Size: 6.1 MB (6124277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa257ea47ccbcf0f4f7fc1790bf5eb92b3a0ae52e1ad2eeab796c971b4d8777`  
		Last Modified: Thu, 11 Jan 2024 02:49:19 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3196725eed73232f06492a1060fdba1af514ac24a95ee83078183e9cd6e93b7`  
		Last Modified: Thu, 11 Jan 2024 02:49:19 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:f64cc78db496614d2464bc518395a9a9c18dcbced888bd246c53a5f607fb2798
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8753027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f43f54a537b58038fca151e541618e03368dcf372994c25b941d20ef6bb6dc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 02:54:55 GMT
ENV NATS_SERVER=2.10.8
# Thu, 11 Jan 2024 02:54:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d74bba93d60a6a9836f4b54e942b8d4c2c9f33855659584cc7f76fdf8b1c4f7' ;; 		armhf) natsArch='arm6'; sha256='63147f419cda88e2d6f508e7a93dcc35803ad07d3a25bd5bdfdf3830f22a096d' ;; 		armv7) natsArch='arm7'; sha256='bc87934be36709f6f8928e5d65c7f11e8e2c5660826aa6c9af87b3a69cb6b8c3' ;; 		x86_64) natsArch='amd64'; sha256='23f647b813f339f0c8c2ac545f75bebcb2821dce0f47eca50e475e44b5d663d9' ;; 		x86) natsArch='386'; sha256='1ae8582969e34ff731bf065c724ad742ba2a1f566ad8de169b87f9e97b52f5ff' ;; 		s390x) natsArch='s390x'; sha256='826735b8333787b27191cf201162398b530f417f2b80f224fefcfa9d21b480c2' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:54:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:54:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:55:00 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:55:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:55:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e8e103dfb44072b9bbf2eba7aad94fd639e561a22768da2bb37ea7d6729bab4`  
		Last Modified: Thu, 11 Jan 2024 02:55:51 GMT  
		Size: 5.8 MB (5833322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6faf32ab3656f6bddf90a09ced2d48b14b852842c566514822d55a40ed52361a`  
		Last Modified: Thu, 11 Jan 2024 02:55:50 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be21811ddbd891a760c2cc348a08f710ae14eeac84aa8d7d5af26c6581efc8e1`  
		Last Modified: Thu, 11 Jan 2024 02:55:49 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9244a34a1c67c86e4f309985a0c9ddc44c4a26dd32201cebc262d1a246f1e2d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9049174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4798f08bfc804e8b7077ab10105d2f686a6204a3f904209ec83f681962ea21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 02:49:45 GMT
ENV NATS_SERVER=2.10.8
# Thu, 11 Jan 2024 02:49:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d74bba93d60a6a9836f4b54e942b8d4c2c9f33855659584cc7f76fdf8b1c4f7' ;; 		armhf) natsArch='arm6'; sha256='63147f419cda88e2d6f508e7a93dcc35803ad07d3a25bd5bdfdf3830f22a096d' ;; 		armv7) natsArch='arm7'; sha256='bc87934be36709f6f8928e5d65c7f11e8e2c5660826aa6c9af87b3a69cb6b8c3' ;; 		x86_64) natsArch='amd64'; sha256='23f647b813f339f0c8c2ac545f75bebcb2821dce0f47eca50e475e44b5d663d9' ;; 		x86) natsArch='386'; sha256='1ae8582969e34ff731bf065c724ad742ba2a1f566ad8de169b87f9e97b52f5ff' ;; 		s390x) natsArch='s390x'; sha256='826735b8333787b27191cf201162398b530f417f2b80f224fefcfa9d21b480c2' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:49:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:49:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:49:48 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:49:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:49:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef2adfa7ed66cbcf98bfd19fd849cab6c342a8bf21efe1c363c1ec5d3c41ae0`  
		Last Modified: Thu, 11 Jan 2024 02:50:22 GMT  
		Size: 5.7 MB (5700378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c865cf9777bd8e4753ce89930261559591a9d2e030c0dbd995f82ba770e06f`  
		Last Modified: Thu, 11 Jan 2024 02:50:21 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1071663058684a0e820ec88c736711fda64c374c9a2492274176aadd0ef9bf83`  
		Last Modified: Thu, 11 Jan 2024 02:50:21 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:57e0b341099f0bd8156f8311f66e5c28cc1f9b0402b983d8dcaac59cf018ac60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10-linux` - linux; amd64

```console
$ docker pull nats@sha256:cfc16611986dc5883f4d27c9085e76910343d967594ee383d0255baeb057db79
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5501382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd357d7a18b1dda228ed5178c5ca385155fb364d30c57ca494ff97c8cd19309`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:48:54 GMT
COPY file:bfe22f1af895b2fc7a50837842688e659c05693b4bf069ba0376ffc69ae697ea in /nats-server 
# Thu, 11 Jan 2024 02:48:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:48:54 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:48:54 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:48:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7acebaf66611006473295971042ce1d190371c2a188cd83ac1294bdcbe941861`  
		Last Modified: Thu, 11 Jan 2024 02:49:55 GMT  
		Size: 5.5 MB (5500874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eaf929d718cd812eb25392358200a35e1e26347e9cfdce5e0b620aa8b735742`  
		Last Modified: Thu, 11 Jan 2024 02:49:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:25e7841f5b4c74faa1cefa3ac3a9b676cde24301bb4457381d45a631aeaed3af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0df98ee98ab731da5630054247a95f41befffd2873016036e7fe10c0f93ddb4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 07 Dec 2023 00:49:31 GMT
COPY file:57db66e8f632416070a8742db1e78e42b6a00178d3cafbb1d951f712bc1528b0 in /nats-server 
# Thu, 07 Dec 2023 00:49:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 07 Dec 2023 00:49:31 GMT
EXPOSE 4222 6222 8222
# Thu, 07 Dec 2023 00:49:31 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 07 Dec 2023 00:49:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dd9254a38d172bab9b5d4a85c3955a5bf8dc94569fdf541322f3006b8087cec0`  
		Last Modified: Thu, 07 Dec 2023 00:50:20 GMT  
		Size: 5.2 MB (5204791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30653da0be2fe0acec3ba9ba2b603cc6aa9511b5d611c70c10ecdd9b0709ad51`  
		Last Modified: Thu, 07 Dec 2023 00:50:19 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:a64d6b7675f0097a69544912df42b5d4e9b121bfff34649843637c53ab640cfb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5210866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3ae88cd2cd670d8b9b7f6e610fd3eb8687d499c38ca124f8033d847bbe8881`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:55:20 GMT
COPY file:8b6480435610d9164cd2c66bf75ef01eb81c3073e740cad17c74339e5baedda5 in /nats-server 
# Thu, 11 Jan 2024 02:55:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:55:21 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:55:21 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:55:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0920770a264f958a57c4e11d9c31cf4441041ea655047f6e857b67fad43906f9`  
		Last Modified: Thu, 11 Jan 2024 02:56:29 GMT  
		Size: 5.2 MB (5210357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c60b3bdf3047e4a3391384685743bd7f58305a89f5c71bd9b22fcd6e30211b`  
		Last Modified: Thu, 11 Jan 2024 02:56:28 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:187bdea269fa2454820b2e7d8e40ff4c70919e9caeac33af047e45e86f4e9118
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e480d5474031fbc4d95f443dc0e87b2d5bcfa6936887c9c20ddc78880966d3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:49:59 GMT
COPY file:8879823466eafef24f1fda27c9cd4f809446ce0288c6939e09932ffe25ab7b19 in /nats-server 
# Thu, 11 Jan 2024 02:50:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:50:00 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:50:00 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:50:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1e7857182cff537484895387bffc3495ec32bd159979fa4d1b851b83d7cd87c3`  
		Last Modified: Thu, 11 Jan 2024 02:50:57 GMT  
		Size: 5.1 MB (5075684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ac1735dae6ad6bb18f1075bbad502a9dc797d686f5c92486bd72aa9c38499e`  
		Last Modified: Thu, 11 Jan 2024 02:50:56 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver`

```console
$ docker pull nats@sha256:decd1f161f484155c8ca7a0c7e99247a35f4cb1b9d297b9f821b6e07246b56a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.10-nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:ee000864a3122839be74300a01091298092421330414b26a5bd46dd177c45413
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110213906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3efb56477e7b9c48586d8290198510d573b31cedd83e0a3ffce9e7e6657e36`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 04:01:12 GMT
RUN cmd /S /C #(nop) COPY file:f6f49d606f9f811d8d95cfcbfc0c7db19c139753cf9d4aec8e19ceb60cae5eb7 in C:\nats-server.exe 
# Thu, 11 Jan 2024 04:01:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 04:01:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 04:01:14 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 04:01:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf42f1aafdb6016daeae38b38330cdd9dc19c174db9d4af6b68dd916e6eb084`  
		Last Modified: Thu, 11 Jan 2024 04:02:15 GMT  
		Size: 5.6 MB (5616337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c327a7a2c7b1f345092bbe2268b1cae828a27ee468658e4fd8894e7e6e66cc`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba577085c3d41035606a7eea09d46f81aa7b7d70cea80113a9f07d14e31ede2b`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506c8f4ceb3d31803fab29316067ffc5129a0d9b9c208f0b52fc86161329769a`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d929e177552db84f77ab4e31fc7399f97d242ff17d7b23874f7ef22d1c912e`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-1809`

```console
$ docker pull nats@sha256:decd1f161f484155c8ca7a0c7e99247a35f4cb1b9d297b9f821b6e07246b56a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.10-nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:ee000864a3122839be74300a01091298092421330414b26a5bd46dd177c45413
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110213906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3efb56477e7b9c48586d8290198510d573b31cedd83e0a3ffce9e7e6657e36`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 04:01:12 GMT
RUN cmd /S /C #(nop) COPY file:f6f49d606f9f811d8d95cfcbfc0c7db19c139753cf9d4aec8e19ceb60cae5eb7 in C:\nats-server.exe 
# Thu, 11 Jan 2024 04:01:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 04:01:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 04:01:14 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 04:01:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf42f1aafdb6016daeae38b38330cdd9dc19c174db9d4af6b68dd916e6eb084`  
		Last Modified: Thu, 11 Jan 2024 04:02:15 GMT  
		Size: 5.6 MB (5616337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c327a7a2c7b1f345092bbe2268b1cae828a27ee468658e4fd8894e7e6e66cc`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba577085c3d41035606a7eea09d46f81aa7b7d70cea80113a9f07d14e31ede2b`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506c8f4ceb3d31803fab29316067ffc5129a0d9b9c208f0b52fc86161329769a`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d929e177552db84f77ab4e31fc7399f97d242ff17d7b23874f7ef22d1c912e`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-scratch`

```console
$ docker pull nats@sha256:57e0b341099f0bd8156f8311f66e5c28cc1f9b0402b983d8dcaac59cf018ac60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10-scratch` - linux; amd64

```console
$ docker pull nats@sha256:cfc16611986dc5883f4d27c9085e76910343d967594ee383d0255baeb057db79
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5501382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd357d7a18b1dda228ed5178c5ca385155fb364d30c57ca494ff97c8cd19309`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:48:54 GMT
COPY file:bfe22f1af895b2fc7a50837842688e659c05693b4bf069ba0376ffc69ae697ea in /nats-server 
# Thu, 11 Jan 2024 02:48:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:48:54 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:48:54 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:48:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7acebaf66611006473295971042ce1d190371c2a188cd83ac1294bdcbe941861`  
		Last Modified: Thu, 11 Jan 2024 02:49:55 GMT  
		Size: 5.5 MB (5500874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eaf929d718cd812eb25392358200a35e1e26347e9cfdce5e0b620aa8b735742`  
		Last Modified: Thu, 11 Jan 2024 02:49:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:25e7841f5b4c74faa1cefa3ac3a9b676cde24301bb4457381d45a631aeaed3af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0df98ee98ab731da5630054247a95f41befffd2873016036e7fe10c0f93ddb4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 07 Dec 2023 00:49:31 GMT
COPY file:57db66e8f632416070a8742db1e78e42b6a00178d3cafbb1d951f712bc1528b0 in /nats-server 
# Thu, 07 Dec 2023 00:49:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 07 Dec 2023 00:49:31 GMT
EXPOSE 4222 6222 8222
# Thu, 07 Dec 2023 00:49:31 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 07 Dec 2023 00:49:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dd9254a38d172bab9b5d4a85c3955a5bf8dc94569fdf541322f3006b8087cec0`  
		Last Modified: Thu, 07 Dec 2023 00:50:20 GMT  
		Size: 5.2 MB (5204791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30653da0be2fe0acec3ba9ba2b603cc6aa9511b5d611c70c10ecdd9b0709ad51`  
		Last Modified: Thu, 07 Dec 2023 00:50:19 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:a64d6b7675f0097a69544912df42b5d4e9b121bfff34649843637c53ab640cfb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5210866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3ae88cd2cd670d8b9b7f6e610fd3eb8687d499c38ca124f8033d847bbe8881`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:55:20 GMT
COPY file:8b6480435610d9164cd2c66bf75ef01eb81c3073e740cad17c74339e5baedda5 in /nats-server 
# Thu, 11 Jan 2024 02:55:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:55:21 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:55:21 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:55:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0920770a264f958a57c4e11d9c31cf4441041ea655047f6e857b67fad43906f9`  
		Last Modified: Thu, 11 Jan 2024 02:56:29 GMT  
		Size: 5.2 MB (5210357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c60b3bdf3047e4a3391384685743bd7f58305a89f5c71bd9b22fcd6e30211b`  
		Last Modified: Thu, 11 Jan 2024 02:56:28 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:187bdea269fa2454820b2e7d8e40ff4c70919e9caeac33af047e45e86f4e9118
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e480d5474031fbc4d95f443dc0e87b2d5bcfa6936887c9c20ddc78880966d3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:49:59 GMT
COPY file:8879823466eafef24f1fda27c9cd4f809446ce0288c6939e09932ffe25ab7b19 in /nats-server 
# Thu, 11 Jan 2024 02:50:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:50:00 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:50:00 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:50:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1e7857182cff537484895387bffc3495ec32bd159979fa4d1b851b83d7cd87c3`  
		Last Modified: Thu, 11 Jan 2024 02:50:57 GMT  
		Size: 5.1 MB (5075684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ac1735dae6ad6bb18f1075bbad502a9dc797d686f5c92486bd72aa9c38499e`  
		Last Modified: Thu, 11 Jan 2024 02:50:56 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore`

```console
$ docker pull nats@sha256:0bff0a4798c7f8bb2f02043d4d61e95f0c76717250d81c9e143d7ab3a2351a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:89f52b8b81a1fbf176205e5cb5caa71f8cc75b4fd9a057eda45eee9d007f0e6b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2076105215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99dc11e338875bec0e0c7c688468d40f6e3262afe6e4ab99858b86e9f2a2ba47`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 03:57:58 GMT
ENV NATS_SERVER=2.10.8
# Thu, 11 Jan 2024 03:57:59 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.8/nats-server-v2.10.8-windows-amd64.zip
# Thu, 11 Jan 2024 03:58:00 GMT
ENV NATS_SERVER_SHASUM=032ed7ebec9d3f40d9b096b005101a3568a2ab07bee93be9db089eef354f3dab
# Thu, 11 Jan 2024 03:59:12 GMT
RUN Set-PSDebug -Trace 2
# Thu, 11 Jan 2024 04:00:54 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 11 Jan 2024 04:00:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 04:00:55 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 04:00:56 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 04:00:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c6e78cb437ea2945136109e2881a48e24e24f66592ba7778be64331e4d2ccb`  
		Last Modified: Thu, 11 Jan 2024 04:01:58 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00914bffce2598259b34ebafa40823fc65864b8b43f937d9e3b7283d16e60f7`  
		Last Modified: Thu, 11 Jan 2024 04:01:58 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751940e3a482a7a84fd7a9741ca18de682fc19b1674c23c2d0d13872e842ed46`  
		Last Modified: Thu, 11 Jan 2024 04:01:58 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0123ebddfd37d224bec740e66f603c2345f82f4c08b38d32fac94721f733b6`  
		Last Modified: Thu, 11 Jan 2024 04:01:59 GMT  
		Size: 457.1 KB (457126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd190f787f1a3f9741dd6f585a98c58e1c0530276b617abccca895fed4e5dbc`  
		Last Modified: Thu, 11 Jan 2024 04:01:58 GMT  
		Size: 5.9 MB (5912649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f6de4df082e15ca15fd484cb3719198ab7ffb70c7e968ec7b20abc6185ad49`  
		Last Modified: Thu, 11 Jan 2024 04:01:56 GMT  
		Size: 1.9 KB (1941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b495bdea1d447e57b8bf347ca127dde4f38a0fbb092e876a032ac6ae3b7282`  
		Last Modified: Thu, 11 Jan 2024 04:01:56 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e041ce5ffd08bbec0256f9a994966ae544af0f4d2c49dc8ea7fff59e508865`  
		Last Modified: Thu, 11 Jan 2024 04:01:56 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d2322a5a4a23d0999899882871e27f86bbfbec89b82d95eac704cb6d02764d`  
		Last Modified: Thu, 11 Jan 2024 04:01:56 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-1809`

```console
$ docker pull nats@sha256:0bff0a4798c7f8bb2f02043d4d61e95f0c76717250d81c9e143d7ab3a2351a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.10-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:89f52b8b81a1fbf176205e5cb5caa71f8cc75b4fd9a057eda45eee9d007f0e6b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2076105215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99dc11e338875bec0e0c7c688468d40f6e3262afe6e4ab99858b86e9f2a2ba47`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 03:57:58 GMT
ENV NATS_SERVER=2.10.8
# Thu, 11 Jan 2024 03:57:59 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.8/nats-server-v2.10.8-windows-amd64.zip
# Thu, 11 Jan 2024 03:58:00 GMT
ENV NATS_SERVER_SHASUM=032ed7ebec9d3f40d9b096b005101a3568a2ab07bee93be9db089eef354f3dab
# Thu, 11 Jan 2024 03:59:12 GMT
RUN Set-PSDebug -Trace 2
# Thu, 11 Jan 2024 04:00:54 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 11 Jan 2024 04:00:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 04:00:55 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 04:00:56 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 04:00:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c6e78cb437ea2945136109e2881a48e24e24f66592ba7778be64331e4d2ccb`  
		Last Modified: Thu, 11 Jan 2024 04:01:58 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00914bffce2598259b34ebafa40823fc65864b8b43f937d9e3b7283d16e60f7`  
		Last Modified: Thu, 11 Jan 2024 04:01:58 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751940e3a482a7a84fd7a9741ca18de682fc19b1674c23c2d0d13872e842ed46`  
		Last Modified: Thu, 11 Jan 2024 04:01:58 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0123ebddfd37d224bec740e66f603c2345f82f4c08b38d32fac94721f733b6`  
		Last Modified: Thu, 11 Jan 2024 04:01:59 GMT  
		Size: 457.1 KB (457126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd190f787f1a3f9741dd6f585a98c58e1c0530276b617abccca895fed4e5dbc`  
		Last Modified: Thu, 11 Jan 2024 04:01:58 GMT  
		Size: 5.9 MB (5912649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f6de4df082e15ca15fd484cb3719198ab7ffb70c7e968ec7b20abc6185ad49`  
		Last Modified: Thu, 11 Jan 2024 04:01:56 GMT  
		Size: 1.9 KB (1941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b495bdea1d447e57b8bf347ca127dde4f38a0fbb092e876a032ac6ae3b7282`  
		Last Modified: Thu, 11 Jan 2024 04:01:56 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e041ce5ffd08bbec0256f9a994966ae544af0f4d2c49dc8ea7fff59e508865`  
		Last Modified: Thu, 11 Jan 2024 04:01:56 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d2322a5a4a23d0999899882871e27f86bbfbec89b82d95eac704cb6d02764d`  
		Last Modified: Thu, 11 Jan 2024 04:01:56 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.8`

```console
$ docker pull nats@sha256:35e0f4869e4fee288b812ce50e86ef14279123652d46921fdccf9d37177a935a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.5329; amd64

### `nats:2.10.8` - linux; amd64

```console
$ docker pull nats@sha256:cfc16611986dc5883f4d27c9085e76910343d967594ee383d0255baeb057db79
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5501382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd357d7a18b1dda228ed5178c5ca385155fb364d30c57ca494ff97c8cd19309`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:48:54 GMT
COPY file:bfe22f1af895b2fc7a50837842688e659c05693b4bf069ba0376ffc69ae697ea in /nats-server 
# Thu, 11 Jan 2024 02:48:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:48:54 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:48:54 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:48:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7acebaf66611006473295971042ce1d190371c2a188cd83ac1294bdcbe941861`  
		Last Modified: Thu, 11 Jan 2024 02:49:55 GMT  
		Size: 5.5 MB (5500874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eaf929d718cd812eb25392358200a35e1e26347e9cfdce5e0b620aa8b735742`  
		Last Modified: Thu, 11 Jan 2024 02:49:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.8` - linux; arm variant v7

```console
$ docker pull nats@sha256:a64d6b7675f0097a69544912df42b5d4e9b121bfff34649843637c53ab640cfb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5210866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3ae88cd2cd670d8b9b7f6e610fd3eb8687d499c38ca124f8033d847bbe8881`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:55:20 GMT
COPY file:8b6480435610d9164cd2c66bf75ef01eb81c3073e740cad17c74339e5baedda5 in /nats-server 
# Thu, 11 Jan 2024 02:55:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:55:21 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:55:21 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:55:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0920770a264f958a57c4e11d9c31cf4441041ea655047f6e857b67fad43906f9`  
		Last Modified: Thu, 11 Jan 2024 02:56:29 GMT  
		Size: 5.2 MB (5210357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c60b3bdf3047e4a3391384685743bd7f58305a89f5c71bd9b22fcd6e30211b`  
		Last Modified: Thu, 11 Jan 2024 02:56:28 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.8` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:187bdea269fa2454820b2e7d8e40ff4c70919e9caeac33af047e45e86f4e9118
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e480d5474031fbc4d95f443dc0e87b2d5bcfa6936887c9c20ddc78880966d3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:49:59 GMT
COPY file:8879823466eafef24f1fda27c9cd4f809446ce0288c6939e09932ffe25ab7b19 in /nats-server 
# Thu, 11 Jan 2024 02:50:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:50:00 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:50:00 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:50:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1e7857182cff537484895387bffc3495ec32bd159979fa4d1b851b83d7cd87c3`  
		Last Modified: Thu, 11 Jan 2024 02:50:57 GMT  
		Size: 5.1 MB (5075684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ac1735dae6ad6bb18f1075bbad502a9dc797d686f5c92486bd72aa9c38499e`  
		Last Modified: Thu, 11 Jan 2024 02:50:56 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.8` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:ee000864a3122839be74300a01091298092421330414b26a5bd46dd177c45413
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110213906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3efb56477e7b9c48586d8290198510d573b31cedd83e0a3ffce9e7e6657e36`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 04:01:12 GMT
RUN cmd /S /C #(nop) COPY file:f6f49d606f9f811d8d95cfcbfc0c7db19c139753cf9d4aec8e19ceb60cae5eb7 in C:\nats-server.exe 
# Thu, 11 Jan 2024 04:01:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 04:01:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 04:01:14 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 04:01:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf42f1aafdb6016daeae38b38330cdd9dc19c174db9d4af6b68dd916e6eb084`  
		Last Modified: Thu, 11 Jan 2024 04:02:15 GMT  
		Size: 5.6 MB (5616337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c327a7a2c7b1f345092bbe2268b1cae828a27ee468658e4fd8894e7e6e66cc`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba577085c3d41035606a7eea09d46f81aa7b7d70cea80113a9f07d14e31ede2b`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506c8f4ceb3d31803fab29316067ffc5129a0d9b9c208f0b52fc86161329769a`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d929e177552db84f77ab4e31fc7399f97d242ff17d7b23874f7ef22d1c912e`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.8-alpine`

```console
$ docker pull nats@sha256:1983fb960c52b05c1b212d459943fb024dac5419eda36bf55bf64279de68499d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10.8-alpine` - linux; amd64

```console
$ docker pull nats@sha256:ea36396a4460389cb144a9022eb5f3ea64591fb8a05f6d5d1a056db30fec8929
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6033b15096c9a633bd78cc2d815e6069d5b0f9f43e2d7208967ba46596f359d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 02:48:35 GMT
ENV NATS_SERVER=2.10.8
# Thu, 11 Jan 2024 02:48:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d74bba93d60a6a9836f4b54e942b8d4c2c9f33855659584cc7f76fdf8b1c4f7' ;; 		armhf) natsArch='arm6'; sha256='63147f419cda88e2d6f508e7a93dcc35803ad07d3a25bd5bdfdf3830f22a096d' ;; 		armv7) natsArch='arm7'; sha256='bc87934be36709f6f8928e5d65c7f11e8e2c5660826aa6c9af87b3a69cb6b8c3' ;; 		x86_64) natsArch='amd64'; sha256='23f647b813f339f0c8c2ac545f75bebcb2821dce0f47eca50e475e44b5d663d9' ;; 		x86) natsArch='386'; sha256='1ae8582969e34ff731bf065c724ad742ba2a1f566ad8de169b87f9e97b52f5ff' ;; 		s390x) natsArch='s390x'; sha256='826735b8333787b27191cf201162398b530f417f2b80f224fefcfa9d21b480c2' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:48:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:48:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:48:37 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:48:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:48:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f798ba46b67098bd15d5e60f4ba21bc7a74dea83bc32e096b2c4a69fcebd1c`  
		Last Modified: Thu, 11 Jan 2024 02:49:20 GMT  
		Size: 6.1 MB (6124277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa257ea47ccbcf0f4f7fc1790bf5eb92b3a0ae52e1ad2eeab796c971b4d8777`  
		Last Modified: Thu, 11 Jan 2024 02:49:19 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3196725eed73232f06492a1060fdba1af514ac24a95ee83078183e9cd6e93b7`  
		Last Modified: Thu, 11 Jan 2024 02:49:19 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.8-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:f64cc78db496614d2464bc518395a9a9c18dcbced888bd246c53a5f607fb2798
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8753027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f43f54a537b58038fca151e541618e03368dcf372994c25b941d20ef6bb6dc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 02:54:55 GMT
ENV NATS_SERVER=2.10.8
# Thu, 11 Jan 2024 02:54:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d74bba93d60a6a9836f4b54e942b8d4c2c9f33855659584cc7f76fdf8b1c4f7' ;; 		armhf) natsArch='arm6'; sha256='63147f419cda88e2d6f508e7a93dcc35803ad07d3a25bd5bdfdf3830f22a096d' ;; 		armv7) natsArch='arm7'; sha256='bc87934be36709f6f8928e5d65c7f11e8e2c5660826aa6c9af87b3a69cb6b8c3' ;; 		x86_64) natsArch='amd64'; sha256='23f647b813f339f0c8c2ac545f75bebcb2821dce0f47eca50e475e44b5d663d9' ;; 		x86) natsArch='386'; sha256='1ae8582969e34ff731bf065c724ad742ba2a1f566ad8de169b87f9e97b52f5ff' ;; 		s390x) natsArch='s390x'; sha256='826735b8333787b27191cf201162398b530f417f2b80f224fefcfa9d21b480c2' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:54:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:54:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:55:00 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:55:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:55:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e8e103dfb44072b9bbf2eba7aad94fd639e561a22768da2bb37ea7d6729bab4`  
		Last Modified: Thu, 11 Jan 2024 02:55:51 GMT  
		Size: 5.8 MB (5833322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6faf32ab3656f6bddf90a09ced2d48b14b852842c566514822d55a40ed52361a`  
		Last Modified: Thu, 11 Jan 2024 02:55:50 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be21811ddbd891a760c2cc348a08f710ae14eeac84aa8d7d5af26c6581efc8e1`  
		Last Modified: Thu, 11 Jan 2024 02:55:49 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.8-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9244a34a1c67c86e4f309985a0c9ddc44c4a26dd32201cebc262d1a246f1e2d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9049174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4798f08bfc804e8b7077ab10105d2f686a6204a3f904209ec83f681962ea21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 02:49:45 GMT
ENV NATS_SERVER=2.10.8
# Thu, 11 Jan 2024 02:49:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d74bba93d60a6a9836f4b54e942b8d4c2c9f33855659584cc7f76fdf8b1c4f7' ;; 		armhf) natsArch='arm6'; sha256='63147f419cda88e2d6f508e7a93dcc35803ad07d3a25bd5bdfdf3830f22a096d' ;; 		armv7) natsArch='arm7'; sha256='bc87934be36709f6f8928e5d65c7f11e8e2c5660826aa6c9af87b3a69cb6b8c3' ;; 		x86_64) natsArch='amd64'; sha256='23f647b813f339f0c8c2ac545f75bebcb2821dce0f47eca50e475e44b5d663d9' ;; 		x86) natsArch='386'; sha256='1ae8582969e34ff731bf065c724ad742ba2a1f566ad8de169b87f9e97b52f5ff' ;; 		s390x) natsArch='s390x'; sha256='826735b8333787b27191cf201162398b530f417f2b80f224fefcfa9d21b480c2' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:49:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:49:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:49:48 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:49:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:49:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef2adfa7ed66cbcf98bfd19fd849cab6c342a8bf21efe1c363c1ec5d3c41ae0`  
		Last Modified: Thu, 11 Jan 2024 02:50:22 GMT  
		Size: 5.7 MB (5700378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c865cf9777bd8e4753ce89930261559591a9d2e030c0dbd995f82ba770e06f`  
		Last Modified: Thu, 11 Jan 2024 02:50:21 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1071663058684a0e820ec88c736711fda64c374c9a2492274176aadd0ef9bf83`  
		Last Modified: Thu, 11 Jan 2024 02:50:21 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.8-alpine3.19`

```console
$ docker pull nats@sha256:1983fb960c52b05c1b212d459943fb024dac5419eda36bf55bf64279de68499d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10.8-alpine3.19` - linux; amd64

```console
$ docker pull nats@sha256:ea36396a4460389cb144a9022eb5f3ea64591fb8a05f6d5d1a056db30fec8929
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6033b15096c9a633bd78cc2d815e6069d5b0f9f43e2d7208967ba46596f359d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 02:48:35 GMT
ENV NATS_SERVER=2.10.8
# Thu, 11 Jan 2024 02:48:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d74bba93d60a6a9836f4b54e942b8d4c2c9f33855659584cc7f76fdf8b1c4f7' ;; 		armhf) natsArch='arm6'; sha256='63147f419cda88e2d6f508e7a93dcc35803ad07d3a25bd5bdfdf3830f22a096d' ;; 		armv7) natsArch='arm7'; sha256='bc87934be36709f6f8928e5d65c7f11e8e2c5660826aa6c9af87b3a69cb6b8c3' ;; 		x86_64) natsArch='amd64'; sha256='23f647b813f339f0c8c2ac545f75bebcb2821dce0f47eca50e475e44b5d663d9' ;; 		x86) natsArch='386'; sha256='1ae8582969e34ff731bf065c724ad742ba2a1f566ad8de169b87f9e97b52f5ff' ;; 		s390x) natsArch='s390x'; sha256='826735b8333787b27191cf201162398b530f417f2b80f224fefcfa9d21b480c2' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:48:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:48:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:48:37 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:48:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:48:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f798ba46b67098bd15d5e60f4ba21bc7a74dea83bc32e096b2c4a69fcebd1c`  
		Last Modified: Thu, 11 Jan 2024 02:49:20 GMT  
		Size: 6.1 MB (6124277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa257ea47ccbcf0f4f7fc1790bf5eb92b3a0ae52e1ad2eeab796c971b4d8777`  
		Last Modified: Thu, 11 Jan 2024 02:49:19 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3196725eed73232f06492a1060fdba1af514ac24a95ee83078183e9cd6e93b7`  
		Last Modified: Thu, 11 Jan 2024 02:49:19 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.8-alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:f64cc78db496614d2464bc518395a9a9c18dcbced888bd246c53a5f607fb2798
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8753027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f43f54a537b58038fca151e541618e03368dcf372994c25b941d20ef6bb6dc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 02:54:55 GMT
ENV NATS_SERVER=2.10.8
# Thu, 11 Jan 2024 02:54:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d74bba93d60a6a9836f4b54e942b8d4c2c9f33855659584cc7f76fdf8b1c4f7' ;; 		armhf) natsArch='arm6'; sha256='63147f419cda88e2d6f508e7a93dcc35803ad07d3a25bd5bdfdf3830f22a096d' ;; 		armv7) natsArch='arm7'; sha256='bc87934be36709f6f8928e5d65c7f11e8e2c5660826aa6c9af87b3a69cb6b8c3' ;; 		x86_64) natsArch='amd64'; sha256='23f647b813f339f0c8c2ac545f75bebcb2821dce0f47eca50e475e44b5d663d9' ;; 		x86) natsArch='386'; sha256='1ae8582969e34ff731bf065c724ad742ba2a1f566ad8de169b87f9e97b52f5ff' ;; 		s390x) natsArch='s390x'; sha256='826735b8333787b27191cf201162398b530f417f2b80f224fefcfa9d21b480c2' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:54:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:54:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:55:00 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:55:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:55:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e8e103dfb44072b9bbf2eba7aad94fd639e561a22768da2bb37ea7d6729bab4`  
		Last Modified: Thu, 11 Jan 2024 02:55:51 GMT  
		Size: 5.8 MB (5833322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6faf32ab3656f6bddf90a09ced2d48b14b852842c566514822d55a40ed52361a`  
		Last Modified: Thu, 11 Jan 2024 02:55:50 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be21811ddbd891a760c2cc348a08f710ae14eeac84aa8d7d5af26c6581efc8e1`  
		Last Modified: Thu, 11 Jan 2024 02:55:49 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.8-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9244a34a1c67c86e4f309985a0c9ddc44c4a26dd32201cebc262d1a246f1e2d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9049174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4798f08bfc804e8b7077ab10105d2f686a6204a3f904209ec83f681962ea21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 02:49:45 GMT
ENV NATS_SERVER=2.10.8
# Thu, 11 Jan 2024 02:49:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d74bba93d60a6a9836f4b54e942b8d4c2c9f33855659584cc7f76fdf8b1c4f7' ;; 		armhf) natsArch='arm6'; sha256='63147f419cda88e2d6f508e7a93dcc35803ad07d3a25bd5bdfdf3830f22a096d' ;; 		armv7) natsArch='arm7'; sha256='bc87934be36709f6f8928e5d65c7f11e8e2c5660826aa6c9af87b3a69cb6b8c3' ;; 		x86_64) natsArch='amd64'; sha256='23f647b813f339f0c8c2ac545f75bebcb2821dce0f47eca50e475e44b5d663d9' ;; 		x86) natsArch='386'; sha256='1ae8582969e34ff731bf065c724ad742ba2a1f566ad8de169b87f9e97b52f5ff' ;; 		s390x) natsArch='s390x'; sha256='826735b8333787b27191cf201162398b530f417f2b80f224fefcfa9d21b480c2' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:49:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:49:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:49:48 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:49:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:49:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef2adfa7ed66cbcf98bfd19fd849cab6c342a8bf21efe1c363c1ec5d3c41ae0`  
		Last Modified: Thu, 11 Jan 2024 02:50:22 GMT  
		Size: 5.7 MB (5700378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c865cf9777bd8e4753ce89930261559591a9d2e030c0dbd995f82ba770e06f`  
		Last Modified: Thu, 11 Jan 2024 02:50:21 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1071663058684a0e820ec88c736711fda64c374c9a2492274176aadd0ef9bf83`  
		Last Modified: Thu, 11 Jan 2024 02:50:21 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.8-linux`

```console
$ docker pull nats@sha256:cbc5e8d4a5ea94eb83ff93a92159e4bb692c6ae13a6994813246711fb1abcf8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10.8-linux` - linux; amd64

```console
$ docker pull nats@sha256:cfc16611986dc5883f4d27c9085e76910343d967594ee383d0255baeb057db79
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5501382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd357d7a18b1dda228ed5178c5ca385155fb364d30c57ca494ff97c8cd19309`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:48:54 GMT
COPY file:bfe22f1af895b2fc7a50837842688e659c05693b4bf069ba0376ffc69ae697ea in /nats-server 
# Thu, 11 Jan 2024 02:48:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:48:54 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:48:54 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:48:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7acebaf66611006473295971042ce1d190371c2a188cd83ac1294bdcbe941861`  
		Last Modified: Thu, 11 Jan 2024 02:49:55 GMT  
		Size: 5.5 MB (5500874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eaf929d718cd812eb25392358200a35e1e26347e9cfdce5e0b620aa8b735742`  
		Last Modified: Thu, 11 Jan 2024 02:49:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.8-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:a64d6b7675f0097a69544912df42b5d4e9b121bfff34649843637c53ab640cfb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5210866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3ae88cd2cd670d8b9b7f6e610fd3eb8687d499c38ca124f8033d847bbe8881`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:55:20 GMT
COPY file:8b6480435610d9164cd2c66bf75ef01eb81c3073e740cad17c74339e5baedda5 in /nats-server 
# Thu, 11 Jan 2024 02:55:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:55:21 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:55:21 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:55:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0920770a264f958a57c4e11d9c31cf4441041ea655047f6e857b67fad43906f9`  
		Last Modified: Thu, 11 Jan 2024 02:56:29 GMT  
		Size: 5.2 MB (5210357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c60b3bdf3047e4a3391384685743bd7f58305a89f5c71bd9b22fcd6e30211b`  
		Last Modified: Thu, 11 Jan 2024 02:56:28 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.8-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:187bdea269fa2454820b2e7d8e40ff4c70919e9caeac33af047e45e86f4e9118
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e480d5474031fbc4d95f443dc0e87b2d5bcfa6936887c9c20ddc78880966d3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:49:59 GMT
COPY file:8879823466eafef24f1fda27c9cd4f809446ce0288c6939e09932ffe25ab7b19 in /nats-server 
# Thu, 11 Jan 2024 02:50:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:50:00 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:50:00 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:50:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1e7857182cff537484895387bffc3495ec32bd159979fa4d1b851b83d7cd87c3`  
		Last Modified: Thu, 11 Jan 2024 02:50:57 GMT  
		Size: 5.1 MB (5075684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ac1735dae6ad6bb18f1075bbad502a9dc797d686f5c92486bd72aa9c38499e`  
		Last Modified: Thu, 11 Jan 2024 02:50:56 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.8-nanoserver`

```console
$ docker pull nats@sha256:decd1f161f484155c8ca7a0c7e99247a35f4cb1b9d297b9f821b6e07246b56a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.10.8-nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:ee000864a3122839be74300a01091298092421330414b26a5bd46dd177c45413
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110213906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3efb56477e7b9c48586d8290198510d573b31cedd83e0a3ffce9e7e6657e36`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 04:01:12 GMT
RUN cmd /S /C #(nop) COPY file:f6f49d606f9f811d8d95cfcbfc0c7db19c139753cf9d4aec8e19ceb60cae5eb7 in C:\nats-server.exe 
# Thu, 11 Jan 2024 04:01:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 04:01:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 04:01:14 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 04:01:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf42f1aafdb6016daeae38b38330cdd9dc19c174db9d4af6b68dd916e6eb084`  
		Last Modified: Thu, 11 Jan 2024 04:02:15 GMT  
		Size: 5.6 MB (5616337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c327a7a2c7b1f345092bbe2268b1cae828a27ee468658e4fd8894e7e6e66cc`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba577085c3d41035606a7eea09d46f81aa7b7d70cea80113a9f07d14e31ede2b`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506c8f4ceb3d31803fab29316067ffc5129a0d9b9c208f0b52fc86161329769a`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d929e177552db84f77ab4e31fc7399f97d242ff17d7b23874f7ef22d1c912e`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.8-nanoserver-1809`

```console
$ docker pull nats@sha256:decd1f161f484155c8ca7a0c7e99247a35f4cb1b9d297b9f821b6e07246b56a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.10.8-nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:ee000864a3122839be74300a01091298092421330414b26a5bd46dd177c45413
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110213906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3efb56477e7b9c48586d8290198510d573b31cedd83e0a3ffce9e7e6657e36`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 04:01:12 GMT
RUN cmd /S /C #(nop) COPY file:f6f49d606f9f811d8d95cfcbfc0c7db19c139753cf9d4aec8e19ceb60cae5eb7 in C:\nats-server.exe 
# Thu, 11 Jan 2024 04:01:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 04:01:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 04:01:14 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 04:01:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf42f1aafdb6016daeae38b38330cdd9dc19c174db9d4af6b68dd916e6eb084`  
		Last Modified: Thu, 11 Jan 2024 04:02:15 GMT  
		Size: 5.6 MB (5616337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c327a7a2c7b1f345092bbe2268b1cae828a27ee468658e4fd8894e7e6e66cc`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba577085c3d41035606a7eea09d46f81aa7b7d70cea80113a9f07d14e31ede2b`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506c8f4ceb3d31803fab29316067ffc5129a0d9b9c208f0b52fc86161329769a`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d929e177552db84f77ab4e31fc7399f97d242ff17d7b23874f7ef22d1c912e`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.8-scratch`

```console
$ docker pull nats@sha256:cbc5e8d4a5ea94eb83ff93a92159e4bb692c6ae13a6994813246711fb1abcf8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10.8-scratch` - linux; amd64

```console
$ docker pull nats@sha256:cfc16611986dc5883f4d27c9085e76910343d967594ee383d0255baeb057db79
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5501382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd357d7a18b1dda228ed5178c5ca385155fb364d30c57ca494ff97c8cd19309`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:48:54 GMT
COPY file:bfe22f1af895b2fc7a50837842688e659c05693b4bf069ba0376ffc69ae697ea in /nats-server 
# Thu, 11 Jan 2024 02:48:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:48:54 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:48:54 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:48:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7acebaf66611006473295971042ce1d190371c2a188cd83ac1294bdcbe941861`  
		Last Modified: Thu, 11 Jan 2024 02:49:55 GMT  
		Size: 5.5 MB (5500874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eaf929d718cd812eb25392358200a35e1e26347e9cfdce5e0b620aa8b735742`  
		Last Modified: Thu, 11 Jan 2024 02:49:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.8-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:a64d6b7675f0097a69544912df42b5d4e9b121bfff34649843637c53ab640cfb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5210866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3ae88cd2cd670d8b9b7f6e610fd3eb8687d499c38ca124f8033d847bbe8881`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:55:20 GMT
COPY file:8b6480435610d9164cd2c66bf75ef01eb81c3073e740cad17c74339e5baedda5 in /nats-server 
# Thu, 11 Jan 2024 02:55:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:55:21 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:55:21 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:55:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0920770a264f958a57c4e11d9c31cf4441041ea655047f6e857b67fad43906f9`  
		Last Modified: Thu, 11 Jan 2024 02:56:29 GMT  
		Size: 5.2 MB (5210357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c60b3bdf3047e4a3391384685743bd7f58305a89f5c71bd9b22fcd6e30211b`  
		Last Modified: Thu, 11 Jan 2024 02:56:28 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.8-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:187bdea269fa2454820b2e7d8e40ff4c70919e9caeac33af047e45e86f4e9118
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e480d5474031fbc4d95f443dc0e87b2d5bcfa6936887c9c20ddc78880966d3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:49:59 GMT
COPY file:8879823466eafef24f1fda27c9cd4f809446ce0288c6939e09932ffe25ab7b19 in /nats-server 
# Thu, 11 Jan 2024 02:50:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:50:00 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:50:00 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:50:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1e7857182cff537484895387bffc3495ec32bd159979fa4d1b851b83d7cd87c3`  
		Last Modified: Thu, 11 Jan 2024 02:50:57 GMT  
		Size: 5.1 MB (5075684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ac1735dae6ad6bb18f1075bbad502a9dc797d686f5c92486bd72aa9c38499e`  
		Last Modified: Thu, 11 Jan 2024 02:50:56 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.8-windowsservercore`

```console
$ docker pull nats@sha256:0bff0a4798c7f8bb2f02043d4d61e95f0c76717250d81c9e143d7ab3a2351a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.10.8-windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:89f52b8b81a1fbf176205e5cb5caa71f8cc75b4fd9a057eda45eee9d007f0e6b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2076105215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99dc11e338875bec0e0c7c688468d40f6e3262afe6e4ab99858b86e9f2a2ba47`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 03:57:58 GMT
ENV NATS_SERVER=2.10.8
# Thu, 11 Jan 2024 03:57:59 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.8/nats-server-v2.10.8-windows-amd64.zip
# Thu, 11 Jan 2024 03:58:00 GMT
ENV NATS_SERVER_SHASUM=032ed7ebec9d3f40d9b096b005101a3568a2ab07bee93be9db089eef354f3dab
# Thu, 11 Jan 2024 03:59:12 GMT
RUN Set-PSDebug -Trace 2
# Thu, 11 Jan 2024 04:00:54 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 11 Jan 2024 04:00:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 04:00:55 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 04:00:56 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 04:00:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c6e78cb437ea2945136109e2881a48e24e24f66592ba7778be64331e4d2ccb`  
		Last Modified: Thu, 11 Jan 2024 04:01:58 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00914bffce2598259b34ebafa40823fc65864b8b43f937d9e3b7283d16e60f7`  
		Last Modified: Thu, 11 Jan 2024 04:01:58 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751940e3a482a7a84fd7a9741ca18de682fc19b1674c23c2d0d13872e842ed46`  
		Last Modified: Thu, 11 Jan 2024 04:01:58 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0123ebddfd37d224bec740e66f603c2345f82f4c08b38d32fac94721f733b6`  
		Last Modified: Thu, 11 Jan 2024 04:01:59 GMT  
		Size: 457.1 KB (457126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd190f787f1a3f9741dd6f585a98c58e1c0530276b617abccca895fed4e5dbc`  
		Last Modified: Thu, 11 Jan 2024 04:01:58 GMT  
		Size: 5.9 MB (5912649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f6de4df082e15ca15fd484cb3719198ab7ffb70c7e968ec7b20abc6185ad49`  
		Last Modified: Thu, 11 Jan 2024 04:01:56 GMT  
		Size: 1.9 KB (1941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b495bdea1d447e57b8bf347ca127dde4f38a0fbb092e876a032ac6ae3b7282`  
		Last Modified: Thu, 11 Jan 2024 04:01:56 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e041ce5ffd08bbec0256f9a994966ae544af0f4d2c49dc8ea7fff59e508865`  
		Last Modified: Thu, 11 Jan 2024 04:01:56 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d2322a5a4a23d0999899882871e27f86bbfbec89b82d95eac704cb6d02764d`  
		Last Modified: Thu, 11 Jan 2024 04:01:56 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.8-windowsservercore-1809`

```console
$ docker pull nats@sha256:0bff0a4798c7f8bb2f02043d4d61e95f0c76717250d81c9e143d7ab3a2351a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.10.8-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:89f52b8b81a1fbf176205e5cb5caa71f8cc75b4fd9a057eda45eee9d007f0e6b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2076105215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99dc11e338875bec0e0c7c688468d40f6e3262afe6e4ab99858b86e9f2a2ba47`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 03:57:58 GMT
ENV NATS_SERVER=2.10.8
# Thu, 11 Jan 2024 03:57:59 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.8/nats-server-v2.10.8-windows-amd64.zip
# Thu, 11 Jan 2024 03:58:00 GMT
ENV NATS_SERVER_SHASUM=032ed7ebec9d3f40d9b096b005101a3568a2ab07bee93be9db089eef354f3dab
# Thu, 11 Jan 2024 03:59:12 GMT
RUN Set-PSDebug -Trace 2
# Thu, 11 Jan 2024 04:00:54 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 11 Jan 2024 04:00:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 04:00:55 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 04:00:56 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 04:00:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c6e78cb437ea2945136109e2881a48e24e24f66592ba7778be64331e4d2ccb`  
		Last Modified: Thu, 11 Jan 2024 04:01:58 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00914bffce2598259b34ebafa40823fc65864b8b43f937d9e3b7283d16e60f7`  
		Last Modified: Thu, 11 Jan 2024 04:01:58 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751940e3a482a7a84fd7a9741ca18de682fc19b1674c23c2d0d13872e842ed46`  
		Last Modified: Thu, 11 Jan 2024 04:01:58 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0123ebddfd37d224bec740e66f603c2345f82f4c08b38d32fac94721f733b6`  
		Last Modified: Thu, 11 Jan 2024 04:01:59 GMT  
		Size: 457.1 KB (457126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd190f787f1a3f9741dd6f585a98c58e1c0530276b617abccca895fed4e5dbc`  
		Last Modified: Thu, 11 Jan 2024 04:01:58 GMT  
		Size: 5.9 MB (5912649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f6de4df082e15ca15fd484cb3719198ab7ffb70c7e968ec7b20abc6185ad49`  
		Last Modified: Thu, 11 Jan 2024 04:01:56 GMT  
		Size: 1.9 KB (1941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b495bdea1d447e57b8bf347ca127dde4f38a0fbb092e876a032ac6ae3b7282`  
		Last Modified: Thu, 11 Jan 2024 04:01:56 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e041ce5ffd08bbec0256f9a994966ae544af0f4d2c49dc8ea7fff59e508865`  
		Last Modified: Thu, 11 Jan 2024 04:01:56 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d2322a5a4a23d0999899882871e27f86bbfbec89b82d95eac704cb6d02764d`  
		Last Modified: Thu, 11 Jan 2024 04:01:56 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9`

```console
$ docker pull nats@sha256:92f7e9aef076cfefd13b8ceee7d3c2e603be5a9751c4fa686b9e1595422d97a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9` - linux; amd64

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

### `nats:2.9` - linux; arm variant v6

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

### `nats:2.9` - linux; arm variant v7

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

### `nats:2.9` - linux; arm64 variant v8

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

## `nats:2.9-alpine`

```console
$ docker pull nats@sha256:19a0f5d2153a0b19c4582e0ce20d8a358d7563dcf037ca03bc93b505c9a5e942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine` - linux; amd64

```console
$ docker pull nats@sha256:876da24b7f4f2dea20b6475670a38024132a19a9a8ad2bd9b628ea2599947d49
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9275205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f52e093e5ec56f688a4ae2de3d596844d9b1edc5385825cdb522ca3a0ecf20c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:09:38 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 02:48:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:48:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:48:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:48:42 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:48:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:48:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e159124713dd6006dd0ece709bd692909269ab6746abf612da09f028632af39`  
		Last Modified: Thu, 11 Jan 2024 02:49:41 GMT  
		Size: 5.9 MB (5871785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac3058ecb44517fdd3bfa721db14ad31124f3fd6ba2ad02bf8a0383f4d8929d`  
		Last Modified: Thu, 11 Jan 2024 02:49:40 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334b353900146652ebc9b4c510737112cd977108f9d005e369a53f8aefd9786b`  
		Last Modified: Thu, 11 Jan 2024 02:49:40 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:ea12096d05d14c61677a950ccecc14fa970228a2f9c32cc9756a34d16e23627e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8755974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421c22f9992da9e131b79a8e00614b62903755a114929c4efeca51d4104147a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 01:11:34 GMT
ENV NATS_SERVER=2.9.24
# Fri, 01 Dec 2023 01:11:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 01 Dec 2023 01:11:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 01 Dec 2023 01:11:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 01 Dec 2023 01:11:37 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Dec 2023 01:11:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 01:11:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d08b1bd7ab7a87de18e67897b423e6b9889387c94e2409d3f50904ec9c4369`  
		Last Modified: Fri, 01 Dec 2023 01:12:26 GMT  
		Size: 5.6 MB (5608105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3e4b8e5ff4da13becde614c85a197b276c30ec0a40344c59375f6560dd0fae`  
		Last Modified: Fri, 01 Dec 2023 01:12:25 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea581f787924f03908f3e60d8c32cf33838817759152d4b770bfdf856f84a5e1`  
		Last Modified: Fri, 01 Dec 2023 01:12:25 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:395e2cca4875e55718f3a57ce4ad85208400418752ddfc421b15dbfdb190d130
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8502426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f55fd5f07b843eba8c33c1c02278f2e67dca10e10d35ff50511dcf5c8b0f00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:40:43 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 02:55:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:55:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:55:08 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:55:08 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:55:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:55:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ac175087690e2968161b68e59a4589097c0cd79c73aa82f9057d626c45f2ef`  
		Last Modified: Thu, 11 Jan 2024 02:56:14 GMT  
		Size: 5.6 MB (5600415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061a37440ace92eb08d27cd402169cbf52185ed748785d926abe7ad52a046882`  
		Last Modified: Thu, 11 Jan 2024 02:56:13 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14eb2e96b94e493297c9d5427d0f73900b5de0cdad3ff8da15996144ed638641`  
		Last Modified: Thu, 11 Jan 2024 02:56:13 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:3c2e18441c62fab8c39fa6995e7f2ca1a036f1e26fe9958e3d227821a95643df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8743651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94d697f5f4c7cfaad04d3bb5ae7ef7128d9fc58a217c3088e755a725fb75f61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:51:49 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 02:49:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:49:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:49:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:49:53 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:49:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:49:53 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab5e72e0eb0c95e7e7fe19fd5edb045b295f214e17a410a6efa51b4696c9e84`  
		Last Modified: Thu, 11 Jan 2024 02:50:43 GMT  
		Size: 5.4 MB (5409617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3cf37be8e997367e307b6c202abc4d97bb507b6973efa2b14b0b1632c6b25bc`  
		Last Modified: Thu, 11 Jan 2024 02:50:42 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3be8724e2044d42784181c3bf1940fd85d692b8cccec5a827f2e46feba9a261`  
		Last Modified: Thu, 11 Jan 2024 02:50:42 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine3.18`

```console
$ docker pull nats@sha256:19a0f5d2153a0b19c4582e0ce20d8a358d7563dcf037ca03bc93b505c9a5e942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:876da24b7f4f2dea20b6475670a38024132a19a9a8ad2bd9b628ea2599947d49
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9275205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f52e093e5ec56f688a4ae2de3d596844d9b1edc5385825cdb522ca3a0ecf20c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:09:38 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 02:48:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:48:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:48:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:48:42 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:48:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:48:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e159124713dd6006dd0ece709bd692909269ab6746abf612da09f028632af39`  
		Last Modified: Thu, 11 Jan 2024 02:49:41 GMT  
		Size: 5.9 MB (5871785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac3058ecb44517fdd3bfa721db14ad31124f3fd6ba2ad02bf8a0383f4d8929d`  
		Last Modified: Thu, 11 Jan 2024 02:49:40 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334b353900146652ebc9b4c510737112cd977108f9d005e369a53f8aefd9786b`  
		Last Modified: Thu, 11 Jan 2024 02:49:40 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:ea12096d05d14c61677a950ccecc14fa970228a2f9c32cc9756a34d16e23627e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8755974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421c22f9992da9e131b79a8e00614b62903755a114929c4efeca51d4104147a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 01:11:34 GMT
ENV NATS_SERVER=2.9.24
# Fri, 01 Dec 2023 01:11:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 01 Dec 2023 01:11:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 01 Dec 2023 01:11:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 01 Dec 2023 01:11:37 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Dec 2023 01:11:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 01:11:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d08b1bd7ab7a87de18e67897b423e6b9889387c94e2409d3f50904ec9c4369`  
		Last Modified: Fri, 01 Dec 2023 01:12:26 GMT  
		Size: 5.6 MB (5608105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3e4b8e5ff4da13becde614c85a197b276c30ec0a40344c59375f6560dd0fae`  
		Last Modified: Fri, 01 Dec 2023 01:12:25 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea581f787924f03908f3e60d8c32cf33838817759152d4b770bfdf856f84a5e1`  
		Last Modified: Fri, 01 Dec 2023 01:12:25 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:395e2cca4875e55718f3a57ce4ad85208400418752ddfc421b15dbfdb190d130
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8502426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f55fd5f07b843eba8c33c1c02278f2e67dca10e10d35ff50511dcf5c8b0f00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:40:43 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 02:55:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:55:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:55:08 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:55:08 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:55:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:55:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ac175087690e2968161b68e59a4589097c0cd79c73aa82f9057d626c45f2ef`  
		Last Modified: Thu, 11 Jan 2024 02:56:14 GMT  
		Size: 5.6 MB (5600415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061a37440ace92eb08d27cd402169cbf52185ed748785d926abe7ad52a046882`  
		Last Modified: Thu, 11 Jan 2024 02:56:13 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14eb2e96b94e493297c9d5427d0f73900b5de0cdad3ff8da15996144ed638641`  
		Last Modified: Thu, 11 Jan 2024 02:56:13 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:3c2e18441c62fab8c39fa6995e7f2ca1a036f1e26fe9958e3d227821a95643df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8743651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94d697f5f4c7cfaad04d3bb5ae7ef7128d9fc58a217c3088e755a725fb75f61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:51:49 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 02:49:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:49:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:49:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:49:53 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:49:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:49:53 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab5e72e0eb0c95e7e7fe19fd5edb045b295f214e17a410a6efa51b4696c9e84`  
		Last Modified: Thu, 11 Jan 2024 02:50:43 GMT  
		Size: 5.4 MB (5409617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3cf37be8e997367e307b6c202abc4d97bb507b6973efa2b14b0b1632c6b25bc`  
		Last Modified: Thu, 11 Jan 2024 02:50:42 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3be8724e2044d42784181c3bf1940fd85d692b8cccec5a827f2e46feba9a261`  
		Last Modified: Thu, 11 Jan 2024 02:50:42 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-linux`

```console
$ docker pull nats@sha256:92f7e9aef076cfefd13b8ceee7d3c2e603be5a9751c4fa686b9e1595422d97a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-linux` - linux; amd64

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

### `nats:2.9-linux` - linux; arm variant v6

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

### `nats:2.9-linux` - linux; arm variant v7

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

### `nats:2.9-linux` - linux; arm64 variant v8

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

## `nats:2.9-nanoserver`

```console
$ docker pull nats@sha256:73e62a60d396fc48da607c6331930fd0805d167c151c01b5bb6d007d6e730e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.9-nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:04dfc0fb7c253ad7cc06425afaf83755a891623745f7d9b4b3c1d26f09f5084e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109926528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f308760511a2d142f4e7e157bcc4aee60a2fddfc8d95068108d571da790394`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:17:15 GMT
RUN cmd /S /C #(nop) COPY file:bb76bb5eb2960343e0d31314ed4649c426ed59ad3d060057e2c1038e39265b76 in C:\nats-server.exe 
# Thu, 11 Jan 2024 00:17:16 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 00:17:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 00:17:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 00:17:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d1a38e007259758a3002c7063aa1d123543275c117035c8cac9ccd30e1f1b0`  
		Last Modified: Thu, 11 Jan 2024 00:18:32 GMT  
		Size: 5.3 MB (5328981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6455e2b47c383137ec2bb5bef5aeb229331027b345c2d08f14135f1ee5d6034`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b09a3551da5ce47e8c7fdc4fd9437b2e46d67f0c5033ac499d4ddb0caaa9e0`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4488ed73414629a19600657dcb357e27539522baf886a146543112d12ecf2db`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0357d2bc4b192b40d9b8b3df99265f3425faa6618d305ab3b5f4a36511932231`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver-1809`

```console
$ docker pull nats@sha256:73e62a60d396fc48da607c6331930fd0805d167c151c01b5bb6d007d6e730e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.9-nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:04dfc0fb7c253ad7cc06425afaf83755a891623745f7d9b4b3c1d26f09f5084e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109926528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f308760511a2d142f4e7e157bcc4aee60a2fddfc8d95068108d571da790394`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:17:15 GMT
RUN cmd /S /C #(nop) COPY file:bb76bb5eb2960343e0d31314ed4649c426ed59ad3d060057e2c1038e39265b76 in C:\nats-server.exe 
# Thu, 11 Jan 2024 00:17:16 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 00:17:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 00:17:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 00:17:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d1a38e007259758a3002c7063aa1d123543275c117035c8cac9ccd30e1f1b0`  
		Last Modified: Thu, 11 Jan 2024 00:18:32 GMT  
		Size: 5.3 MB (5328981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6455e2b47c383137ec2bb5bef5aeb229331027b345c2d08f14135f1ee5d6034`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b09a3551da5ce47e8c7fdc4fd9437b2e46d67f0c5033ac499d4ddb0caaa9e0`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4488ed73414629a19600657dcb357e27539522baf886a146543112d12ecf2db`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0357d2bc4b192b40d9b8b3df99265f3425faa6618d305ab3b5f4a36511932231`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-scratch`

```console
$ docker pull nats@sha256:92f7e9aef076cfefd13b8ceee7d3c2e603be5a9751c4fa686b9e1595422d97a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-scratch` - linux; amd64

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

### `nats:2.9-scratch` - linux; arm variant v6

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

### `nats:2.9-scratch` - linux; arm variant v7

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

### `nats:2.9-scratch` - linux; arm64 variant v8

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

## `nats:2.9-windowsservercore`

```console
$ docker pull nats@sha256:905254cad870fc2919e872296294e54bf7ab513d6400d455504c0ca0eec98fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.9-windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:75d21e7c7902eb91f89a5405f4c0e5b7a3329c3652cd114bb43321f563c300bf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2075790613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97920b4526f302e30dbb8562fa9dd559fff513b660f872a04105dbf48264c14f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:14:14 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 00:14:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.24/nats-server-v2.9.24-windows-amd64.zip
# Thu, 11 Jan 2024 00:14:15 GMT
ENV NATS_SERVER_SHASUM=4caa027910bfa0a79f2d1c01739e356df37dae15f1336174d459d2fd3a0e10d2
# Thu, 11 Jan 2024 00:15:16 GMT
RUN Set-PSDebug -Trace 2
# Thu, 11 Jan 2024 00:16:53 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 11 Jan 2024 00:16:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 00:16:54 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 00:16:55 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 00:16:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce4036858212ca6f064e29e285b6d9fa03ce15b2a9315733365884fb0e63ef4`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d277b320c347208832277f2419ff434f7d3eb54c141aaef2fd13edbef678d3`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1496adc4ee5773352f6bd338210c71dc187b00d620c569f428499f0f210b9be3`  
		Last Modified: Thu, 11 Jan 2024 00:18:21 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df4c9701f2982452fad8368df4c07858b3a1a092c8c62bcb8cd913758a6f7f8`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 442.1 KB (442147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52f7ad94a16aaa3c2af8e25e185081bff82045acef35ae26a038eb262ddbb02`  
		Last Modified: Thu, 11 Jan 2024 00:18:21 GMT  
		Size: 5.6 MB (5612769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c4995bb7eee3d4871a429d8322314cde4e0ff81e5cb749c764fca7cf92c1d7`  
		Last Modified: Thu, 11 Jan 2024 00:18:20 GMT  
		Size: 2.0 KB (1971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24195e2989aa1fdc7ac3c1085f171f29d2418b5359cca044a76edcfafbbea931`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec415c56b7d4247a28d70321f2f0aaee60eb69b2bfdb33070cb41849604beea`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa158ee5a6da454f8f86c48b302e4e3641d718fc212d085e5fe5e5a07856cf4`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore-1809`

```console
$ docker pull nats@sha256:905254cad870fc2919e872296294e54bf7ab513d6400d455504c0ca0eec98fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.9-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:75d21e7c7902eb91f89a5405f4c0e5b7a3329c3652cd114bb43321f563c300bf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2075790613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97920b4526f302e30dbb8562fa9dd559fff513b660f872a04105dbf48264c14f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:14:14 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 00:14:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.24/nats-server-v2.9.24-windows-amd64.zip
# Thu, 11 Jan 2024 00:14:15 GMT
ENV NATS_SERVER_SHASUM=4caa027910bfa0a79f2d1c01739e356df37dae15f1336174d459d2fd3a0e10d2
# Thu, 11 Jan 2024 00:15:16 GMT
RUN Set-PSDebug -Trace 2
# Thu, 11 Jan 2024 00:16:53 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 11 Jan 2024 00:16:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 00:16:54 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 00:16:55 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 00:16:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce4036858212ca6f064e29e285b6d9fa03ce15b2a9315733365884fb0e63ef4`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d277b320c347208832277f2419ff434f7d3eb54c141aaef2fd13edbef678d3`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1496adc4ee5773352f6bd338210c71dc187b00d620c569f428499f0f210b9be3`  
		Last Modified: Thu, 11 Jan 2024 00:18:21 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df4c9701f2982452fad8368df4c07858b3a1a092c8c62bcb8cd913758a6f7f8`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 442.1 KB (442147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52f7ad94a16aaa3c2af8e25e185081bff82045acef35ae26a038eb262ddbb02`  
		Last Modified: Thu, 11 Jan 2024 00:18:21 GMT  
		Size: 5.6 MB (5612769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c4995bb7eee3d4871a429d8322314cde4e0ff81e5cb749c764fca7cf92c1d7`  
		Last Modified: Thu, 11 Jan 2024 00:18:20 GMT  
		Size: 2.0 KB (1971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24195e2989aa1fdc7ac3c1085f171f29d2418b5359cca044a76edcfafbbea931`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec415c56b7d4247a28d70321f2f0aaee60eb69b2bfdb33070cb41849604beea`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa158ee5a6da454f8f86c48b302e4e3641d718fc212d085e5fe5e5a07856cf4`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.24`

```console
$ docker pull nats@sha256:92f7e9aef076cfefd13b8ceee7d3c2e603be5a9751c4fa686b9e1595422d97a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.24` - linux; amd64

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

### `nats:2.9.24` - linux; arm variant v6

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

### `nats:2.9.24` - linux; arm variant v7

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

### `nats:2.9.24` - linux; arm64 variant v8

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

## `nats:2.9.24-alpine`

```console
$ docker pull nats@sha256:19a0f5d2153a0b19c4582e0ce20d8a358d7563dcf037ca03bc93b505c9a5e942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.24-alpine` - linux; amd64

```console
$ docker pull nats@sha256:876da24b7f4f2dea20b6475670a38024132a19a9a8ad2bd9b628ea2599947d49
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9275205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f52e093e5ec56f688a4ae2de3d596844d9b1edc5385825cdb522ca3a0ecf20c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:09:38 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 02:48:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:48:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:48:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:48:42 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:48:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:48:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e159124713dd6006dd0ece709bd692909269ab6746abf612da09f028632af39`  
		Last Modified: Thu, 11 Jan 2024 02:49:41 GMT  
		Size: 5.9 MB (5871785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac3058ecb44517fdd3bfa721db14ad31124f3fd6ba2ad02bf8a0383f4d8929d`  
		Last Modified: Thu, 11 Jan 2024 02:49:40 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334b353900146652ebc9b4c510737112cd977108f9d005e369a53f8aefd9786b`  
		Last Modified: Thu, 11 Jan 2024 02:49:40 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:ea12096d05d14c61677a950ccecc14fa970228a2f9c32cc9756a34d16e23627e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8755974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421c22f9992da9e131b79a8e00614b62903755a114929c4efeca51d4104147a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 01:11:34 GMT
ENV NATS_SERVER=2.9.24
# Fri, 01 Dec 2023 01:11:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 01 Dec 2023 01:11:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 01 Dec 2023 01:11:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 01 Dec 2023 01:11:37 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Dec 2023 01:11:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 01:11:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d08b1bd7ab7a87de18e67897b423e6b9889387c94e2409d3f50904ec9c4369`  
		Last Modified: Fri, 01 Dec 2023 01:12:26 GMT  
		Size: 5.6 MB (5608105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3e4b8e5ff4da13becde614c85a197b276c30ec0a40344c59375f6560dd0fae`  
		Last Modified: Fri, 01 Dec 2023 01:12:25 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea581f787924f03908f3e60d8c32cf33838817759152d4b770bfdf856f84a5e1`  
		Last Modified: Fri, 01 Dec 2023 01:12:25 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:395e2cca4875e55718f3a57ce4ad85208400418752ddfc421b15dbfdb190d130
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8502426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f55fd5f07b843eba8c33c1c02278f2e67dca10e10d35ff50511dcf5c8b0f00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:40:43 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 02:55:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:55:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:55:08 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:55:08 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:55:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:55:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ac175087690e2968161b68e59a4589097c0cd79c73aa82f9057d626c45f2ef`  
		Last Modified: Thu, 11 Jan 2024 02:56:14 GMT  
		Size: 5.6 MB (5600415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061a37440ace92eb08d27cd402169cbf52185ed748785d926abe7ad52a046882`  
		Last Modified: Thu, 11 Jan 2024 02:56:13 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14eb2e96b94e493297c9d5427d0f73900b5de0cdad3ff8da15996144ed638641`  
		Last Modified: Thu, 11 Jan 2024 02:56:13 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:3c2e18441c62fab8c39fa6995e7f2ca1a036f1e26fe9958e3d227821a95643df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8743651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94d697f5f4c7cfaad04d3bb5ae7ef7128d9fc58a217c3088e755a725fb75f61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:51:49 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 02:49:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:49:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:49:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:49:53 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:49:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:49:53 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab5e72e0eb0c95e7e7fe19fd5edb045b295f214e17a410a6efa51b4696c9e84`  
		Last Modified: Thu, 11 Jan 2024 02:50:43 GMT  
		Size: 5.4 MB (5409617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3cf37be8e997367e307b6c202abc4d97bb507b6973efa2b14b0b1632c6b25bc`  
		Last Modified: Thu, 11 Jan 2024 02:50:42 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3be8724e2044d42784181c3bf1940fd85d692b8cccec5a827f2e46feba9a261`  
		Last Modified: Thu, 11 Jan 2024 02:50:42 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.24-alpine3.18`

```console
$ docker pull nats@sha256:19a0f5d2153a0b19c4582e0ce20d8a358d7563dcf037ca03bc93b505c9a5e942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.24-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:876da24b7f4f2dea20b6475670a38024132a19a9a8ad2bd9b628ea2599947d49
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9275205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f52e093e5ec56f688a4ae2de3d596844d9b1edc5385825cdb522ca3a0ecf20c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:09:38 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 02:48:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:48:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:48:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:48:42 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:48:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:48:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e159124713dd6006dd0ece709bd692909269ab6746abf612da09f028632af39`  
		Last Modified: Thu, 11 Jan 2024 02:49:41 GMT  
		Size: 5.9 MB (5871785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac3058ecb44517fdd3bfa721db14ad31124f3fd6ba2ad02bf8a0383f4d8929d`  
		Last Modified: Thu, 11 Jan 2024 02:49:40 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334b353900146652ebc9b4c510737112cd977108f9d005e369a53f8aefd9786b`  
		Last Modified: Thu, 11 Jan 2024 02:49:40 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:ea12096d05d14c61677a950ccecc14fa970228a2f9c32cc9756a34d16e23627e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8755974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421c22f9992da9e131b79a8e00614b62903755a114929c4efeca51d4104147a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 01:11:34 GMT
ENV NATS_SERVER=2.9.24
# Fri, 01 Dec 2023 01:11:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 01 Dec 2023 01:11:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 01 Dec 2023 01:11:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 01 Dec 2023 01:11:37 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Dec 2023 01:11:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 01:11:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d08b1bd7ab7a87de18e67897b423e6b9889387c94e2409d3f50904ec9c4369`  
		Last Modified: Fri, 01 Dec 2023 01:12:26 GMT  
		Size: 5.6 MB (5608105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3e4b8e5ff4da13becde614c85a197b276c30ec0a40344c59375f6560dd0fae`  
		Last Modified: Fri, 01 Dec 2023 01:12:25 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea581f787924f03908f3e60d8c32cf33838817759152d4b770bfdf856f84a5e1`  
		Last Modified: Fri, 01 Dec 2023 01:12:25 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:395e2cca4875e55718f3a57ce4ad85208400418752ddfc421b15dbfdb190d130
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8502426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f55fd5f07b843eba8c33c1c02278f2e67dca10e10d35ff50511dcf5c8b0f00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:40:43 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 02:55:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:55:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:55:08 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:55:08 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:55:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:55:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ac175087690e2968161b68e59a4589097c0cd79c73aa82f9057d626c45f2ef`  
		Last Modified: Thu, 11 Jan 2024 02:56:14 GMT  
		Size: 5.6 MB (5600415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061a37440ace92eb08d27cd402169cbf52185ed748785d926abe7ad52a046882`  
		Last Modified: Thu, 11 Jan 2024 02:56:13 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14eb2e96b94e493297c9d5427d0f73900b5de0cdad3ff8da15996144ed638641`  
		Last Modified: Thu, 11 Jan 2024 02:56:13 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:3c2e18441c62fab8c39fa6995e7f2ca1a036f1e26fe9958e3d227821a95643df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8743651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94d697f5f4c7cfaad04d3bb5ae7ef7128d9fc58a217c3088e755a725fb75f61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:51:49 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 02:49:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:49:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:49:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:49:53 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:49:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:49:53 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab5e72e0eb0c95e7e7fe19fd5edb045b295f214e17a410a6efa51b4696c9e84`  
		Last Modified: Thu, 11 Jan 2024 02:50:43 GMT  
		Size: 5.4 MB (5409617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3cf37be8e997367e307b6c202abc4d97bb507b6973efa2b14b0b1632c6b25bc`  
		Last Modified: Thu, 11 Jan 2024 02:50:42 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3be8724e2044d42784181c3bf1940fd85d692b8cccec5a827f2e46feba9a261`  
		Last Modified: Thu, 11 Jan 2024 02:50:42 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.24-linux`

```console
$ docker pull nats@sha256:92f7e9aef076cfefd13b8ceee7d3c2e603be5a9751c4fa686b9e1595422d97a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.24-linux` - linux; amd64

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

### `nats:2.9.24-linux` - linux; arm variant v6

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

### `nats:2.9.24-linux` - linux; arm variant v7

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

### `nats:2.9.24-linux` - linux; arm64 variant v8

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

## `nats:2.9.24-nanoserver`

```console
$ docker pull nats@sha256:73e62a60d396fc48da607c6331930fd0805d167c151c01b5bb6d007d6e730e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.9.24-nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:04dfc0fb7c253ad7cc06425afaf83755a891623745f7d9b4b3c1d26f09f5084e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109926528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f308760511a2d142f4e7e157bcc4aee60a2fddfc8d95068108d571da790394`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:17:15 GMT
RUN cmd /S /C #(nop) COPY file:bb76bb5eb2960343e0d31314ed4649c426ed59ad3d060057e2c1038e39265b76 in C:\nats-server.exe 
# Thu, 11 Jan 2024 00:17:16 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 00:17:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 00:17:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 00:17:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d1a38e007259758a3002c7063aa1d123543275c117035c8cac9ccd30e1f1b0`  
		Last Modified: Thu, 11 Jan 2024 00:18:32 GMT  
		Size: 5.3 MB (5328981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6455e2b47c383137ec2bb5bef5aeb229331027b345c2d08f14135f1ee5d6034`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b09a3551da5ce47e8c7fdc4fd9437b2e46d67f0c5033ac499d4ddb0caaa9e0`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4488ed73414629a19600657dcb357e27539522baf886a146543112d12ecf2db`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0357d2bc4b192b40d9b8b3df99265f3425faa6618d305ab3b5f4a36511932231`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.24-nanoserver-1809`

```console
$ docker pull nats@sha256:73e62a60d396fc48da607c6331930fd0805d167c151c01b5bb6d007d6e730e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.9.24-nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:04dfc0fb7c253ad7cc06425afaf83755a891623745f7d9b4b3c1d26f09f5084e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109926528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f308760511a2d142f4e7e157bcc4aee60a2fddfc8d95068108d571da790394`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:17:15 GMT
RUN cmd /S /C #(nop) COPY file:bb76bb5eb2960343e0d31314ed4649c426ed59ad3d060057e2c1038e39265b76 in C:\nats-server.exe 
# Thu, 11 Jan 2024 00:17:16 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 00:17:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 00:17:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 00:17:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d1a38e007259758a3002c7063aa1d123543275c117035c8cac9ccd30e1f1b0`  
		Last Modified: Thu, 11 Jan 2024 00:18:32 GMT  
		Size: 5.3 MB (5328981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6455e2b47c383137ec2bb5bef5aeb229331027b345c2d08f14135f1ee5d6034`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b09a3551da5ce47e8c7fdc4fd9437b2e46d67f0c5033ac499d4ddb0caaa9e0`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4488ed73414629a19600657dcb357e27539522baf886a146543112d12ecf2db`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0357d2bc4b192b40d9b8b3df99265f3425faa6618d305ab3b5f4a36511932231`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.24-scratch`

```console
$ docker pull nats@sha256:92f7e9aef076cfefd13b8ceee7d3c2e603be5a9751c4fa686b9e1595422d97a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.24-scratch` - linux; amd64

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

### `nats:2.9.24-scratch` - linux; arm variant v6

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

### `nats:2.9.24-scratch` - linux; arm variant v7

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

### `nats:2.9.24-scratch` - linux; arm64 variant v8

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

## `nats:2.9.24-windowsservercore`

```console
$ docker pull nats@sha256:905254cad870fc2919e872296294e54bf7ab513d6400d455504c0ca0eec98fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.9.24-windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:75d21e7c7902eb91f89a5405f4c0e5b7a3329c3652cd114bb43321f563c300bf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2075790613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97920b4526f302e30dbb8562fa9dd559fff513b660f872a04105dbf48264c14f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:14:14 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 00:14:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.24/nats-server-v2.9.24-windows-amd64.zip
# Thu, 11 Jan 2024 00:14:15 GMT
ENV NATS_SERVER_SHASUM=4caa027910bfa0a79f2d1c01739e356df37dae15f1336174d459d2fd3a0e10d2
# Thu, 11 Jan 2024 00:15:16 GMT
RUN Set-PSDebug -Trace 2
# Thu, 11 Jan 2024 00:16:53 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 11 Jan 2024 00:16:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 00:16:54 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 00:16:55 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 00:16:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce4036858212ca6f064e29e285b6d9fa03ce15b2a9315733365884fb0e63ef4`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d277b320c347208832277f2419ff434f7d3eb54c141aaef2fd13edbef678d3`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1496adc4ee5773352f6bd338210c71dc187b00d620c569f428499f0f210b9be3`  
		Last Modified: Thu, 11 Jan 2024 00:18:21 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df4c9701f2982452fad8368df4c07858b3a1a092c8c62bcb8cd913758a6f7f8`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 442.1 KB (442147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52f7ad94a16aaa3c2af8e25e185081bff82045acef35ae26a038eb262ddbb02`  
		Last Modified: Thu, 11 Jan 2024 00:18:21 GMT  
		Size: 5.6 MB (5612769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c4995bb7eee3d4871a429d8322314cde4e0ff81e5cb749c764fca7cf92c1d7`  
		Last Modified: Thu, 11 Jan 2024 00:18:20 GMT  
		Size: 2.0 KB (1971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24195e2989aa1fdc7ac3c1085f171f29d2418b5359cca044a76edcfafbbea931`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec415c56b7d4247a28d70321f2f0aaee60eb69b2bfdb33070cb41849604beea`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa158ee5a6da454f8f86c48b302e4e3641d718fc212d085e5fe5e5a07856cf4`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.24-windowsservercore-1809`

```console
$ docker pull nats@sha256:905254cad870fc2919e872296294e54bf7ab513d6400d455504c0ca0eec98fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.9.24-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:75d21e7c7902eb91f89a5405f4c0e5b7a3329c3652cd114bb43321f563c300bf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2075790613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97920b4526f302e30dbb8562fa9dd559fff513b660f872a04105dbf48264c14f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:14:14 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 00:14:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.24/nats-server-v2.9.24-windows-amd64.zip
# Thu, 11 Jan 2024 00:14:15 GMT
ENV NATS_SERVER_SHASUM=4caa027910bfa0a79f2d1c01739e356df37dae15f1336174d459d2fd3a0e10d2
# Thu, 11 Jan 2024 00:15:16 GMT
RUN Set-PSDebug -Trace 2
# Thu, 11 Jan 2024 00:16:53 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 11 Jan 2024 00:16:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 00:16:54 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 00:16:55 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 00:16:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce4036858212ca6f064e29e285b6d9fa03ce15b2a9315733365884fb0e63ef4`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d277b320c347208832277f2419ff434f7d3eb54c141aaef2fd13edbef678d3`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1496adc4ee5773352f6bd338210c71dc187b00d620c569f428499f0f210b9be3`  
		Last Modified: Thu, 11 Jan 2024 00:18:21 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df4c9701f2982452fad8368df4c07858b3a1a092c8c62bcb8cd913758a6f7f8`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 442.1 KB (442147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52f7ad94a16aaa3c2af8e25e185081bff82045acef35ae26a038eb262ddbb02`  
		Last Modified: Thu, 11 Jan 2024 00:18:21 GMT  
		Size: 5.6 MB (5612769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c4995bb7eee3d4871a429d8322314cde4e0ff81e5cb749c764fca7cf92c1d7`  
		Last Modified: Thu, 11 Jan 2024 00:18:20 GMT  
		Size: 2.0 KB (1971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24195e2989aa1fdc7ac3c1085f171f29d2418b5359cca044a76edcfafbbea931`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec415c56b7d4247a28d70321f2f0aaee60eb69b2bfdb33070cb41849604beea`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa158ee5a6da454f8f86c48b302e4e3641d718fc212d085e5fe5e5a07856cf4`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:35944c790dd59d33564fe85c8d5ae3085f2ffc0e38ee37254eeeb1a9cc5b9112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:ea36396a4460389cb144a9022eb5f3ea64591fb8a05f6d5d1a056db30fec8929
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6033b15096c9a633bd78cc2d815e6069d5b0f9f43e2d7208967ba46596f359d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 02:48:35 GMT
ENV NATS_SERVER=2.10.8
# Thu, 11 Jan 2024 02:48:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d74bba93d60a6a9836f4b54e942b8d4c2c9f33855659584cc7f76fdf8b1c4f7' ;; 		armhf) natsArch='arm6'; sha256='63147f419cda88e2d6f508e7a93dcc35803ad07d3a25bd5bdfdf3830f22a096d' ;; 		armv7) natsArch='arm7'; sha256='bc87934be36709f6f8928e5d65c7f11e8e2c5660826aa6c9af87b3a69cb6b8c3' ;; 		x86_64) natsArch='amd64'; sha256='23f647b813f339f0c8c2ac545f75bebcb2821dce0f47eca50e475e44b5d663d9' ;; 		x86) natsArch='386'; sha256='1ae8582969e34ff731bf065c724ad742ba2a1f566ad8de169b87f9e97b52f5ff' ;; 		s390x) natsArch='s390x'; sha256='826735b8333787b27191cf201162398b530f417f2b80f224fefcfa9d21b480c2' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:48:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:48:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:48:37 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:48:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:48:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f798ba46b67098bd15d5e60f4ba21bc7a74dea83bc32e096b2c4a69fcebd1c`  
		Last Modified: Thu, 11 Jan 2024 02:49:20 GMT  
		Size: 6.1 MB (6124277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa257ea47ccbcf0f4f7fc1790bf5eb92b3a0ae52e1ad2eeab796c971b4d8777`  
		Last Modified: Thu, 11 Jan 2024 02:49:19 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3196725eed73232f06492a1060fdba1af514ac24a95ee83078183e9cd6e93b7`  
		Last Modified: Thu, 11 Jan 2024 02:49:19 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:5646f5ce83a2cd0809dd62b9103aba3eff6bca2666965032ae01c1425f4c01c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8975747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17c0157045551d25e73637159044fae84067bde183e05d0099b9b806299b456`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Thu, 07 Dec 2023 00:49:19 GMT
ENV NATS_SERVER=2.10.7
# Thu, 07 Dec 2023 00:49:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='9a88afab7b3805475ff7250649447d8807dd52262011252e7faedec926d01782' ;; 		armhf) natsArch='arm6'; sha256='37f8d913cdc69143edf8bd20bceced053b90dba26d1fa94e2e07b6fe17f9db2e' ;; 		armv7) natsArch='arm7'; sha256='d96042f12ecc0578d193d5353c362a572384c6ad9a46db73b7cb5f28cb6e4ad2' ;; 		x86_64) natsArch='amd64'; sha256='91f5b493ce3151baa0b15d8bf093279dc94106dd56a201704a20de567607bcf7' ;; 		x86) natsArch='386'; sha256='a5cddcac9f8debaf45e7b9ba3960778b1c786020c690991094ce31d033ec7649' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 07 Dec 2023 00:49:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 07 Dec 2023 00:49:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 07 Dec 2023 00:49:22 GMT
EXPOSE 4222 6222 8222
# Thu, 07 Dec 2023 00:49:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Dec 2023 00:49:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733b743b5e93d5fde059f514131d51e22a1a4eef1fe4e71d4e42c7fdfc960da9`  
		Last Modified: Thu, 07 Dec 2023 00:49:56 GMT  
		Size: 5.8 MB (5827875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3b83a38bf1009764f2673fbcfe66e38ba7d57492c7838790e767319e64c961`  
		Last Modified: Thu, 07 Dec 2023 00:49:54 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b6d8395d698e101d9e4936dee08916549133753cd0672eceac8ddf1190193a`  
		Last Modified: Thu, 07 Dec 2023 00:49:54 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:f64cc78db496614d2464bc518395a9a9c18dcbced888bd246c53a5f607fb2798
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8753027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f43f54a537b58038fca151e541618e03368dcf372994c25b941d20ef6bb6dc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 02:54:55 GMT
ENV NATS_SERVER=2.10.8
# Thu, 11 Jan 2024 02:54:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d74bba93d60a6a9836f4b54e942b8d4c2c9f33855659584cc7f76fdf8b1c4f7' ;; 		armhf) natsArch='arm6'; sha256='63147f419cda88e2d6f508e7a93dcc35803ad07d3a25bd5bdfdf3830f22a096d' ;; 		armv7) natsArch='arm7'; sha256='bc87934be36709f6f8928e5d65c7f11e8e2c5660826aa6c9af87b3a69cb6b8c3' ;; 		x86_64) natsArch='amd64'; sha256='23f647b813f339f0c8c2ac545f75bebcb2821dce0f47eca50e475e44b5d663d9' ;; 		x86) natsArch='386'; sha256='1ae8582969e34ff731bf065c724ad742ba2a1f566ad8de169b87f9e97b52f5ff' ;; 		s390x) natsArch='s390x'; sha256='826735b8333787b27191cf201162398b530f417f2b80f224fefcfa9d21b480c2' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:54:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:54:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:55:00 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:55:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:55:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e8e103dfb44072b9bbf2eba7aad94fd639e561a22768da2bb37ea7d6729bab4`  
		Last Modified: Thu, 11 Jan 2024 02:55:51 GMT  
		Size: 5.8 MB (5833322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6faf32ab3656f6bddf90a09ced2d48b14b852842c566514822d55a40ed52361a`  
		Last Modified: Thu, 11 Jan 2024 02:55:50 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be21811ddbd891a760c2cc348a08f710ae14eeac84aa8d7d5af26c6581efc8e1`  
		Last Modified: Thu, 11 Jan 2024 02:55:49 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9244a34a1c67c86e4f309985a0c9ddc44c4a26dd32201cebc262d1a246f1e2d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9049174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4798f08bfc804e8b7077ab10105d2f686a6204a3f904209ec83f681962ea21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 02:49:45 GMT
ENV NATS_SERVER=2.10.8
# Thu, 11 Jan 2024 02:49:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d74bba93d60a6a9836f4b54e942b8d4c2c9f33855659584cc7f76fdf8b1c4f7' ;; 		armhf) natsArch='arm6'; sha256='63147f419cda88e2d6f508e7a93dcc35803ad07d3a25bd5bdfdf3830f22a096d' ;; 		armv7) natsArch='arm7'; sha256='bc87934be36709f6f8928e5d65c7f11e8e2c5660826aa6c9af87b3a69cb6b8c3' ;; 		x86_64) natsArch='amd64'; sha256='23f647b813f339f0c8c2ac545f75bebcb2821dce0f47eca50e475e44b5d663d9' ;; 		x86) natsArch='386'; sha256='1ae8582969e34ff731bf065c724ad742ba2a1f566ad8de169b87f9e97b52f5ff' ;; 		s390x) natsArch='s390x'; sha256='826735b8333787b27191cf201162398b530f417f2b80f224fefcfa9d21b480c2' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:49:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:49:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:49:48 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:49:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:49:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef2adfa7ed66cbcf98bfd19fd849cab6c342a8bf21efe1c363c1ec5d3c41ae0`  
		Last Modified: Thu, 11 Jan 2024 02:50:22 GMT  
		Size: 5.7 MB (5700378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c865cf9777bd8e4753ce89930261559591a9d2e030c0dbd995f82ba770e06f`  
		Last Modified: Thu, 11 Jan 2024 02:50:21 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1071663058684a0e820ec88c736711fda64c374c9a2492274176aadd0ef9bf83`  
		Last Modified: Thu, 11 Jan 2024 02:50:21 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.19`

```console
$ docker pull nats@sha256:1983fb960c52b05c1b212d459943fb024dac5419eda36bf55bf64279de68499d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine3.19` - linux; amd64

```console
$ docker pull nats@sha256:ea36396a4460389cb144a9022eb5f3ea64591fb8a05f6d5d1a056db30fec8929
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6033b15096c9a633bd78cc2d815e6069d5b0f9f43e2d7208967ba46596f359d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 02:48:35 GMT
ENV NATS_SERVER=2.10.8
# Thu, 11 Jan 2024 02:48:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d74bba93d60a6a9836f4b54e942b8d4c2c9f33855659584cc7f76fdf8b1c4f7' ;; 		armhf) natsArch='arm6'; sha256='63147f419cda88e2d6f508e7a93dcc35803ad07d3a25bd5bdfdf3830f22a096d' ;; 		armv7) natsArch='arm7'; sha256='bc87934be36709f6f8928e5d65c7f11e8e2c5660826aa6c9af87b3a69cb6b8c3' ;; 		x86_64) natsArch='amd64'; sha256='23f647b813f339f0c8c2ac545f75bebcb2821dce0f47eca50e475e44b5d663d9' ;; 		x86) natsArch='386'; sha256='1ae8582969e34ff731bf065c724ad742ba2a1f566ad8de169b87f9e97b52f5ff' ;; 		s390x) natsArch='s390x'; sha256='826735b8333787b27191cf201162398b530f417f2b80f224fefcfa9d21b480c2' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:48:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:48:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:48:37 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:48:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:48:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f798ba46b67098bd15d5e60f4ba21bc7a74dea83bc32e096b2c4a69fcebd1c`  
		Last Modified: Thu, 11 Jan 2024 02:49:20 GMT  
		Size: 6.1 MB (6124277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa257ea47ccbcf0f4f7fc1790bf5eb92b3a0ae52e1ad2eeab796c971b4d8777`  
		Last Modified: Thu, 11 Jan 2024 02:49:19 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3196725eed73232f06492a1060fdba1af514ac24a95ee83078183e9cd6e93b7`  
		Last Modified: Thu, 11 Jan 2024 02:49:19 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:f64cc78db496614d2464bc518395a9a9c18dcbced888bd246c53a5f607fb2798
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8753027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f43f54a537b58038fca151e541618e03368dcf372994c25b941d20ef6bb6dc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 02:54:55 GMT
ENV NATS_SERVER=2.10.8
# Thu, 11 Jan 2024 02:54:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d74bba93d60a6a9836f4b54e942b8d4c2c9f33855659584cc7f76fdf8b1c4f7' ;; 		armhf) natsArch='arm6'; sha256='63147f419cda88e2d6f508e7a93dcc35803ad07d3a25bd5bdfdf3830f22a096d' ;; 		armv7) natsArch='arm7'; sha256='bc87934be36709f6f8928e5d65c7f11e8e2c5660826aa6c9af87b3a69cb6b8c3' ;; 		x86_64) natsArch='amd64'; sha256='23f647b813f339f0c8c2ac545f75bebcb2821dce0f47eca50e475e44b5d663d9' ;; 		x86) natsArch='386'; sha256='1ae8582969e34ff731bf065c724ad742ba2a1f566ad8de169b87f9e97b52f5ff' ;; 		s390x) natsArch='s390x'; sha256='826735b8333787b27191cf201162398b530f417f2b80f224fefcfa9d21b480c2' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:54:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:54:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:55:00 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:55:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:55:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e8e103dfb44072b9bbf2eba7aad94fd639e561a22768da2bb37ea7d6729bab4`  
		Last Modified: Thu, 11 Jan 2024 02:55:51 GMT  
		Size: 5.8 MB (5833322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6faf32ab3656f6bddf90a09ced2d48b14b852842c566514822d55a40ed52361a`  
		Last Modified: Thu, 11 Jan 2024 02:55:50 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be21811ddbd891a760c2cc348a08f710ae14eeac84aa8d7d5af26c6581efc8e1`  
		Last Modified: Thu, 11 Jan 2024 02:55:49 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9244a34a1c67c86e4f309985a0c9ddc44c4a26dd32201cebc262d1a246f1e2d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9049174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4798f08bfc804e8b7077ab10105d2f686a6204a3f904209ec83f681962ea21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 02:49:45 GMT
ENV NATS_SERVER=2.10.8
# Thu, 11 Jan 2024 02:49:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d74bba93d60a6a9836f4b54e942b8d4c2c9f33855659584cc7f76fdf8b1c4f7' ;; 		armhf) natsArch='arm6'; sha256='63147f419cda88e2d6f508e7a93dcc35803ad07d3a25bd5bdfdf3830f22a096d' ;; 		armv7) natsArch='arm7'; sha256='bc87934be36709f6f8928e5d65c7f11e8e2c5660826aa6c9af87b3a69cb6b8c3' ;; 		x86_64) natsArch='amd64'; sha256='23f647b813f339f0c8c2ac545f75bebcb2821dce0f47eca50e475e44b5d663d9' ;; 		x86) natsArch='386'; sha256='1ae8582969e34ff731bf065c724ad742ba2a1f566ad8de169b87f9e97b52f5ff' ;; 		s390x) natsArch='s390x'; sha256='826735b8333787b27191cf201162398b530f417f2b80f224fefcfa9d21b480c2' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:49:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:49:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:49:48 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:49:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:49:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef2adfa7ed66cbcf98bfd19fd849cab6c342a8bf21efe1c363c1ec5d3c41ae0`  
		Last Modified: Thu, 11 Jan 2024 02:50:22 GMT  
		Size: 5.7 MB (5700378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c865cf9777bd8e4753ce89930261559591a9d2e030c0dbd995f82ba770e06f`  
		Last Modified: Thu, 11 Jan 2024 02:50:21 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1071663058684a0e820ec88c736711fda64c374c9a2492274176aadd0ef9bf83`  
		Last Modified: Thu, 11 Jan 2024 02:50:21 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:bb9953704534e9f6a24a0345cfdda0f4c3c66cf7bcb04dd7dda86ffc16894ac1
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
	-	windows version 10.0.17763.5329; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:cfc16611986dc5883f4d27c9085e76910343d967594ee383d0255baeb057db79
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5501382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd357d7a18b1dda228ed5178c5ca385155fb364d30c57ca494ff97c8cd19309`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:48:54 GMT
COPY file:bfe22f1af895b2fc7a50837842688e659c05693b4bf069ba0376ffc69ae697ea in /nats-server 
# Thu, 11 Jan 2024 02:48:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:48:54 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:48:54 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:48:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7acebaf66611006473295971042ce1d190371c2a188cd83ac1294bdcbe941861`  
		Last Modified: Thu, 11 Jan 2024 02:49:55 GMT  
		Size: 5.5 MB (5500874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eaf929d718cd812eb25392358200a35e1e26347e9cfdce5e0b620aa8b735742`  
		Last Modified: Thu, 11 Jan 2024 02:49:54 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:25e7841f5b4c74faa1cefa3ac3a9b676cde24301bb4457381d45a631aeaed3af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0df98ee98ab731da5630054247a95f41befffd2873016036e7fe10c0f93ddb4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 07 Dec 2023 00:49:31 GMT
COPY file:57db66e8f632416070a8742db1e78e42b6a00178d3cafbb1d951f712bc1528b0 in /nats-server 
# Thu, 07 Dec 2023 00:49:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 07 Dec 2023 00:49:31 GMT
EXPOSE 4222 6222 8222
# Thu, 07 Dec 2023 00:49:31 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 07 Dec 2023 00:49:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dd9254a38d172bab9b5d4a85c3955a5bf8dc94569fdf541322f3006b8087cec0`  
		Last Modified: Thu, 07 Dec 2023 00:50:20 GMT  
		Size: 5.2 MB (5204791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30653da0be2fe0acec3ba9ba2b603cc6aa9511b5d611c70c10ecdd9b0709ad51`  
		Last Modified: Thu, 07 Dec 2023 00:50:19 GMT  
		Size: 509.0 B  
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
$ docker pull nats@sha256:a64d6b7675f0097a69544912df42b5d4e9b121bfff34649843637c53ab640cfb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5210866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3ae88cd2cd670d8b9b7f6e610fd3eb8687d499c38ca124f8033d847bbe8881`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:55:20 GMT
COPY file:8b6480435610d9164cd2c66bf75ef01eb81c3073e740cad17c74339e5baedda5 in /nats-server 
# Thu, 11 Jan 2024 02:55:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:55:21 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:55:21 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:55:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0920770a264f958a57c4e11d9c31cf4441041ea655047f6e857b67fad43906f9`  
		Last Modified: Thu, 11 Jan 2024 02:56:29 GMT  
		Size: 5.2 MB (5210357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c60b3bdf3047e4a3391384685743bd7f58305a89f5c71bd9b22fcd6e30211b`  
		Last Modified: Thu, 11 Jan 2024 02:56:28 GMT  
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
$ docker pull nats@sha256:187bdea269fa2454820b2e7d8e40ff4c70919e9caeac33af047e45e86f4e9118
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e480d5474031fbc4d95f443dc0e87b2d5bcfa6936887c9c20ddc78880966d3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:49:59 GMT
COPY file:8879823466eafef24f1fda27c9cd4f809446ce0288c6939e09932ffe25ab7b19 in /nats-server 
# Thu, 11 Jan 2024 02:50:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:50:00 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:50:00 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:50:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1e7857182cff537484895387bffc3495ec32bd159979fa4d1b851b83d7cd87c3`  
		Last Modified: Thu, 11 Jan 2024 02:50:57 GMT  
		Size: 5.1 MB (5075684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ac1735dae6ad6bb18f1075bbad502a9dc797d686f5c92486bd72aa9c38499e`  
		Last Modified: Thu, 11 Jan 2024 02:50:56 GMT  
		Size: 508.0 B  
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

### `nats:latest` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:ee000864a3122839be74300a01091298092421330414b26a5bd46dd177c45413
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110213906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3efb56477e7b9c48586d8290198510d573b31cedd83e0a3ffce9e7e6657e36`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 04:01:12 GMT
RUN cmd /S /C #(nop) COPY file:f6f49d606f9f811d8d95cfcbfc0c7db19c139753cf9d4aec8e19ceb60cae5eb7 in C:\nats-server.exe 
# Thu, 11 Jan 2024 04:01:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 04:01:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 04:01:14 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 04:01:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf42f1aafdb6016daeae38b38330cdd9dc19c174db9d4af6b68dd916e6eb084`  
		Last Modified: Thu, 11 Jan 2024 04:02:15 GMT  
		Size: 5.6 MB (5616337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c327a7a2c7b1f345092bbe2268b1cae828a27ee468658e4fd8894e7e6e66cc`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba577085c3d41035606a7eea09d46f81aa7b7d70cea80113a9f07d14e31ede2b`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506c8f4ceb3d31803fab29316067ffc5129a0d9b9c208f0b52fc86161329769a`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d929e177552db84f77ab4e31fc7399f97d242ff17d7b23874f7ef22d1c912e`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:57e0b341099f0bd8156f8311f66e5c28cc1f9b0402b983d8dcaac59cf018ac60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:cfc16611986dc5883f4d27c9085e76910343d967594ee383d0255baeb057db79
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5501382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd357d7a18b1dda228ed5178c5ca385155fb364d30c57ca494ff97c8cd19309`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:48:54 GMT
COPY file:bfe22f1af895b2fc7a50837842688e659c05693b4bf069ba0376ffc69ae697ea in /nats-server 
# Thu, 11 Jan 2024 02:48:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:48:54 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:48:54 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:48:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7acebaf66611006473295971042ce1d190371c2a188cd83ac1294bdcbe941861`  
		Last Modified: Thu, 11 Jan 2024 02:49:55 GMT  
		Size: 5.5 MB (5500874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eaf929d718cd812eb25392358200a35e1e26347e9cfdce5e0b620aa8b735742`  
		Last Modified: Thu, 11 Jan 2024 02:49:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:25e7841f5b4c74faa1cefa3ac3a9b676cde24301bb4457381d45a631aeaed3af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0df98ee98ab731da5630054247a95f41befffd2873016036e7fe10c0f93ddb4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 07 Dec 2023 00:49:31 GMT
COPY file:57db66e8f632416070a8742db1e78e42b6a00178d3cafbb1d951f712bc1528b0 in /nats-server 
# Thu, 07 Dec 2023 00:49:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 07 Dec 2023 00:49:31 GMT
EXPOSE 4222 6222 8222
# Thu, 07 Dec 2023 00:49:31 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 07 Dec 2023 00:49:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dd9254a38d172bab9b5d4a85c3955a5bf8dc94569fdf541322f3006b8087cec0`  
		Last Modified: Thu, 07 Dec 2023 00:50:20 GMT  
		Size: 5.2 MB (5204791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30653da0be2fe0acec3ba9ba2b603cc6aa9511b5d611c70c10ecdd9b0709ad51`  
		Last Modified: Thu, 07 Dec 2023 00:50:19 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:a64d6b7675f0097a69544912df42b5d4e9b121bfff34649843637c53ab640cfb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5210866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3ae88cd2cd670d8b9b7f6e610fd3eb8687d499c38ca124f8033d847bbe8881`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:55:20 GMT
COPY file:8b6480435610d9164cd2c66bf75ef01eb81c3073e740cad17c74339e5baedda5 in /nats-server 
# Thu, 11 Jan 2024 02:55:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:55:21 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:55:21 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:55:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0920770a264f958a57c4e11d9c31cf4441041ea655047f6e857b67fad43906f9`  
		Last Modified: Thu, 11 Jan 2024 02:56:29 GMT  
		Size: 5.2 MB (5210357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c60b3bdf3047e4a3391384685743bd7f58305a89f5c71bd9b22fcd6e30211b`  
		Last Modified: Thu, 11 Jan 2024 02:56:28 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:187bdea269fa2454820b2e7d8e40ff4c70919e9caeac33af047e45e86f4e9118
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e480d5474031fbc4d95f443dc0e87b2d5bcfa6936887c9c20ddc78880966d3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:49:59 GMT
COPY file:8879823466eafef24f1fda27c9cd4f809446ce0288c6939e09932ffe25ab7b19 in /nats-server 
# Thu, 11 Jan 2024 02:50:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:50:00 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:50:00 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:50:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1e7857182cff537484895387bffc3495ec32bd159979fa4d1b851b83d7cd87c3`  
		Last Modified: Thu, 11 Jan 2024 02:50:57 GMT  
		Size: 5.1 MB (5075684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ac1735dae6ad6bb18f1075bbad502a9dc797d686f5c92486bd72aa9c38499e`  
		Last Modified: Thu, 11 Jan 2024 02:50:56 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:decd1f161f484155c8ca7a0c7e99247a35f4cb1b9d297b9f821b6e07246b56a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:ee000864a3122839be74300a01091298092421330414b26a5bd46dd177c45413
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110213906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3efb56477e7b9c48586d8290198510d573b31cedd83e0a3ffce9e7e6657e36`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 04:01:12 GMT
RUN cmd /S /C #(nop) COPY file:f6f49d606f9f811d8d95cfcbfc0c7db19c139753cf9d4aec8e19ceb60cae5eb7 in C:\nats-server.exe 
# Thu, 11 Jan 2024 04:01:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 04:01:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 04:01:14 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 04:01:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf42f1aafdb6016daeae38b38330cdd9dc19c174db9d4af6b68dd916e6eb084`  
		Last Modified: Thu, 11 Jan 2024 04:02:15 GMT  
		Size: 5.6 MB (5616337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c327a7a2c7b1f345092bbe2268b1cae828a27ee468658e4fd8894e7e6e66cc`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba577085c3d41035606a7eea09d46f81aa7b7d70cea80113a9f07d14e31ede2b`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506c8f4ceb3d31803fab29316067ffc5129a0d9b9c208f0b52fc86161329769a`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d929e177552db84f77ab4e31fc7399f97d242ff17d7b23874f7ef22d1c912e`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:decd1f161f484155c8ca7a0c7e99247a35f4cb1b9d297b9f821b6e07246b56a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:ee000864a3122839be74300a01091298092421330414b26a5bd46dd177c45413
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110213906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3efb56477e7b9c48586d8290198510d573b31cedd83e0a3ffce9e7e6657e36`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 04:01:12 GMT
RUN cmd /S /C #(nop) COPY file:f6f49d606f9f811d8d95cfcbfc0c7db19c139753cf9d4aec8e19ceb60cae5eb7 in C:\nats-server.exe 
# Thu, 11 Jan 2024 04:01:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 04:01:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 04:01:14 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 04:01:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf42f1aafdb6016daeae38b38330cdd9dc19c174db9d4af6b68dd916e6eb084`  
		Last Modified: Thu, 11 Jan 2024 04:02:15 GMT  
		Size: 5.6 MB (5616337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c327a7a2c7b1f345092bbe2268b1cae828a27ee468658e4fd8894e7e6e66cc`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba577085c3d41035606a7eea09d46f81aa7b7d70cea80113a9f07d14e31ede2b`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506c8f4ceb3d31803fab29316067ffc5129a0d9b9c208f0b52fc86161329769a`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d929e177552db84f77ab4e31fc7399f97d242ff17d7b23874f7ef22d1c912e`  
		Last Modified: Thu, 11 Jan 2024 04:02:13 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:57e0b341099f0bd8156f8311f66e5c28cc1f9b0402b983d8dcaac59cf018ac60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:cfc16611986dc5883f4d27c9085e76910343d967594ee383d0255baeb057db79
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5501382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd357d7a18b1dda228ed5178c5ca385155fb364d30c57ca494ff97c8cd19309`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:48:54 GMT
COPY file:bfe22f1af895b2fc7a50837842688e659c05693b4bf069ba0376ffc69ae697ea in /nats-server 
# Thu, 11 Jan 2024 02:48:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:48:54 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:48:54 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:48:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7acebaf66611006473295971042ce1d190371c2a188cd83ac1294bdcbe941861`  
		Last Modified: Thu, 11 Jan 2024 02:49:55 GMT  
		Size: 5.5 MB (5500874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eaf929d718cd812eb25392358200a35e1e26347e9cfdce5e0b620aa8b735742`  
		Last Modified: Thu, 11 Jan 2024 02:49:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:25e7841f5b4c74faa1cefa3ac3a9b676cde24301bb4457381d45a631aeaed3af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0df98ee98ab731da5630054247a95f41befffd2873016036e7fe10c0f93ddb4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 07 Dec 2023 00:49:31 GMT
COPY file:57db66e8f632416070a8742db1e78e42b6a00178d3cafbb1d951f712bc1528b0 in /nats-server 
# Thu, 07 Dec 2023 00:49:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 07 Dec 2023 00:49:31 GMT
EXPOSE 4222 6222 8222
# Thu, 07 Dec 2023 00:49:31 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 07 Dec 2023 00:49:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dd9254a38d172bab9b5d4a85c3955a5bf8dc94569fdf541322f3006b8087cec0`  
		Last Modified: Thu, 07 Dec 2023 00:50:20 GMT  
		Size: 5.2 MB (5204791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30653da0be2fe0acec3ba9ba2b603cc6aa9511b5d611c70c10ecdd9b0709ad51`  
		Last Modified: Thu, 07 Dec 2023 00:50:19 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:a64d6b7675f0097a69544912df42b5d4e9b121bfff34649843637c53ab640cfb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5210866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3ae88cd2cd670d8b9b7f6e610fd3eb8687d499c38ca124f8033d847bbe8881`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:55:20 GMT
COPY file:8b6480435610d9164cd2c66bf75ef01eb81c3073e740cad17c74339e5baedda5 in /nats-server 
# Thu, 11 Jan 2024 02:55:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:55:21 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:55:21 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:55:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0920770a264f958a57c4e11d9c31cf4441041ea655047f6e857b67fad43906f9`  
		Last Modified: Thu, 11 Jan 2024 02:56:29 GMT  
		Size: 5.2 MB (5210357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c60b3bdf3047e4a3391384685743bd7f58305a89f5c71bd9b22fcd6e30211b`  
		Last Modified: Thu, 11 Jan 2024 02:56:28 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:187bdea269fa2454820b2e7d8e40ff4c70919e9caeac33af047e45e86f4e9118
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e480d5474031fbc4d95f443dc0e87b2d5bcfa6936887c9c20ddc78880966d3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:49:59 GMT
COPY file:8879823466eafef24f1fda27c9cd4f809446ce0288c6939e09932ffe25ab7b19 in /nats-server 
# Thu, 11 Jan 2024 02:50:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:50:00 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:50:00 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:50:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1e7857182cff537484895387bffc3495ec32bd159979fa4d1b851b83d7cd87c3`  
		Last Modified: Thu, 11 Jan 2024 02:50:57 GMT  
		Size: 5.1 MB (5075684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ac1735dae6ad6bb18f1075bbad502a9dc797d686f5c92486bd72aa9c38499e`  
		Last Modified: Thu, 11 Jan 2024 02:50:56 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:0bff0a4798c7f8bb2f02043d4d61e95f0c76717250d81c9e143d7ab3a2351a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:89f52b8b81a1fbf176205e5cb5caa71f8cc75b4fd9a057eda45eee9d007f0e6b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2076105215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99dc11e338875bec0e0c7c688468d40f6e3262afe6e4ab99858b86e9f2a2ba47`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 03:57:58 GMT
ENV NATS_SERVER=2.10.8
# Thu, 11 Jan 2024 03:57:59 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.8/nats-server-v2.10.8-windows-amd64.zip
# Thu, 11 Jan 2024 03:58:00 GMT
ENV NATS_SERVER_SHASUM=032ed7ebec9d3f40d9b096b005101a3568a2ab07bee93be9db089eef354f3dab
# Thu, 11 Jan 2024 03:59:12 GMT
RUN Set-PSDebug -Trace 2
# Thu, 11 Jan 2024 04:00:54 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 11 Jan 2024 04:00:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 04:00:55 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 04:00:56 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 04:00:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c6e78cb437ea2945136109e2881a48e24e24f66592ba7778be64331e4d2ccb`  
		Last Modified: Thu, 11 Jan 2024 04:01:58 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00914bffce2598259b34ebafa40823fc65864b8b43f937d9e3b7283d16e60f7`  
		Last Modified: Thu, 11 Jan 2024 04:01:58 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751940e3a482a7a84fd7a9741ca18de682fc19b1674c23c2d0d13872e842ed46`  
		Last Modified: Thu, 11 Jan 2024 04:01:58 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0123ebddfd37d224bec740e66f603c2345f82f4c08b38d32fac94721f733b6`  
		Last Modified: Thu, 11 Jan 2024 04:01:59 GMT  
		Size: 457.1 KB (457126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd190f787f1a3f9741dd6f585a98c58e1c0530276b617abccca895fed4e5dbc`  
		Last Modified: Thu, 11 Jan 2024 04:01:58 GMT  
		Size: 5.9 MB (5912649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f6de4df082e15ca15fd484cb3719198ab7ffb70c7e968ec7b20abc6185ad49`  
		Last Modified: Thu, 11 Jan 2024 04:01:56 GMT  
		Size: 1.9 KB (1941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b495bdea1d447e57b8bf347ca127dde4f38a0fbb092e876a032ac6ae3b7282`  
		Last Modified: Thu, 11 Jan 2024 04:01:56 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e041ce5ffd08bbec0256f9a994966ae544af0f4d2c49dc8ea7fff59e508865`  
		Last Modified: Thu, 11 Jan 2024 04:01:56 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d2322a5a4a23d0999899882871e27f86bbfbec89b82d95eac704cb6d02764d`  
		Last Modified: Thu, 11 Jan 2024 04:01:56 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:0bff0a4798c7f8bb2f02043d4d61e95f0c76717250d81c9e143d7ab3a2351a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:89f52b8b81a1fbf176205e5cb5caa71f8cc75b4fd9a057eda45eee9d007f0e6b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2076105215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99dc11e338875bec0e0c7c688468d40f6e3262afe6e4ab99858b86e9f2a2ba47`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 03:57:58 GMT
ENV NATS_SERVER=2.10.8
# Thu, 11 Jan 2024 03:57:59 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.8/nats-server-v2.10.8-windows-amd64.zip
# Thu, 11 Jan 2024 03:58:00 GMT
ENV NATS_SERVER_SHASUM=032ed7ebec9d3f40d9b096b005101a3568a2ab07bee93be9db089eef354f3dab
# Thu, 11 Jan 2024 03:59:12 GMT
RUN Set-PSDebug -Trace 2
# Thu, 11 Jan 2024 04:00:54 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 11 Jan 2024 04:00:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 04:00:55 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 04:00:56 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 04:00:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c6e78cb437ea2945136109e2881a48e24e24f66592ba7778be64331e4d2ccb`  
		Last Modified: Thu, 11 Jan 2024 04:01:58 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00914bffce2598259b34ebafa40823fc65864b8b43f937d9e3b7283d16e60f7`  
		Last Modified: Thu, 11 Jan 2024 04:01:58 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751940e3a482a7a84fd7a9741ca18de682fc19b1674c23c2d0d13872e842ed46`  
		Last Modified: Thu, 11 Jan 2024 04:01:58 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0123ebddfd37d224bec740e66f603c2345f82f4c08b38d32fac94721f733b6`  
		Last Modified: Thu, 11 Jan 2024 04:01:59 GMT  
		Size: 457.1 KB (457126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd190f787f1a3f9741dd6f585a98c58e1c0530276b617abccca895fed4e5dbc`  
		Last Modified: Thu, 11 Jan 2024 04:01:58 GMT  
		Size: 5.9 MB (5912649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f6de4df082e15ca15fd484cb3719198ab7ffb70c7e968ec7b20abc6185ad49`  
		Last Modified: Thu, 11 Jan 2024 04:01:56 GMT  
		Size: 1.9 KB (1941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b495bdea1d447e57b8bf347ca127dde4f38a0fbb092e876a032ac6ae3b7282`  
		Last Modified: Thu, 11 Jan 2024 04:01:56 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e041ce5ffd08bbec0256f9a994966ae544af0f4d2c49dc8ea7fff59e508865`  
		Last Modified: Thu, 11 Jan 2024 04:01:56 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d2322a5a4a23d0999899882871e27f86bbfbec89b82d95eac704cb6d02764d`  
		Last Modified: Thu, 11 Jan 2024 04:01:56 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
