## `nats:scratch`

```console
$ docker pull nats@sha256:fe7d14fe1abdebfeeab64a0adad60901ebb262752a9ee763d7298da02cda532b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:dd112e9509fbcc21f21356b82206449cb48a7b738c9f111e591a7a1449c723e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6551634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63bc79c8f8822a03233919198ecbe792b6699f5e1e065c16e563d9b1fbc7a62a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 30 Sep 2025 15:44:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 30 Sep 2025 15:44:04 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 30 Sep 2025 15:44:04 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 30 Sep 2025 15:44:04 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 30 Sep 2025 15:44:04 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 30 Sep 2025 15:44:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b25d31aea6d8978df78bf76b4c1f09e5e69d340de0a2325659ca8237d8341225`  
		Last Modified: Mon, 22 Sep 2025 12:55:07 GMT  
		Size: 6.6 MB (6551124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980881cc39399a931d2b34c68ed7316e7a435ac6b84233c0745df7b96c8c1deb`  
		Last Modified: Wed, 08 Oct 2025 23:33:08 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9031ef2b4d6c7d8489e4c08c87e309dd22131708e7ab6642eadbd369b953eae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1eb4a8463516b6080c4043ba266d62300c6d33a49afb4c428006a4922e98c6`

```dockerfile
```

-	Layers:
	-	`sha256:c1b57215eb3d74de4c8d685be1c5cb7884e60fb07ea371ea1a0045148eef1561`  
		Last Modified: Thu, 09 Oct 2025 02:56:18 GMT  
		Size: 10.5 KB (10464 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:481ba113d1f4d4d2bd34f10913e520860fc835d207d300d29e0be746c1264879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6275102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7dfbd90adb09b8e20dd59a3e1bfb43853276fbd5ca143581bb29f280cf1468b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 30 Sep 2025 15:44:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 30 Sep 2025 15:44:04 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 30 Sep 2025 15:44:04 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 30 Sep 2025 15:44:04 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 30 Sep 2025 15:44:04 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 30 Sep 2025 15:44:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:933ece407f6b99cfe79780c29af3d0c56b8f1bf67f0f9dff449acd262159e005`  
		Last Modified: Mon, 22 Sep 2025 20:38:58 GMT  
		Size: 6.3 MB (6274592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c82f577ea113f404c939c573ed880665deeb47799a706f6068d9d96c0410601`  
		Last Modified: Wed, 08 Oct 2025 22:56:22 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:c8630943ea6a7caacb4d330759408de34378b7726839bd89837892d8cb71e33c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5c37e5871a31671b51d376be50aa9babcb449735ca85144d74daba4851ccfa`

```dockerfile
```

-	Layers:
	-	`sha256:a8d7379995fddc85d7fa859daa0c8ffaebaac814bab3a0def5d028b94bc4bb41`  
		Last Modified: Wed, 08 Oct 2025 23:56:25 GMT  
		Size: 10.6 KB (10597 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:6464d3669aaeab473d87b8843fe4843475cbf9bda6f0ec295bb6f4cb978e23d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6266722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d500e4677c1923a0983f613f34ba05823239956f3a3d28b680355f97bf561f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 30 Sep 2025 15:44:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 30 Sep 2025 15:44:04 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 30 Sep 2025 15:44:04 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 30 Sep 2025 15:44:04 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 30 Sep 2025 15:44:04 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 30 Sep 2025 15:44:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:679a7d604a9c8b13f4291e13da152928a70007f6b7b83b3d057271b6125f6b03`  
		Last Modified: Mon, 22 Sep 2025 20:57:08 GMT  
		Size: 6.3 MB (6266212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9121a98c9c820c8ce14e1c173d232f8ed34cbb7cc095496799931cd4f6a8fb08`  
		Last Modified: Wed, 08 Oct 2025 23:14:22 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:33a2d8ad1d0096d8cbdd8bd04650c587fa87b2128aab3c49faad68d773535bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf8dab31816d369ed9035e21781f2d9c0684fe0ab1d207b6cdf881ec4de1854`

```dockerfile
```

-	Layers:
	-	`sha256:91e1367cb0426aea56e06849768c5fd1e14656beb5c708dda3814892dd22180b`  
		Last Modified: Wed, 08 Oct 2025 23:56:28 GMT  
		Size: 10.6 KB (10597 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:859308b29e6774fd0e1800aa668eb1d99f1002e380a20afa99f25c50579ab1ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5968426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b59e975fc5e842c11454f2b04f617d361149a7946caca96862bb88458d9ae0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 30 Sep 2025 15:44:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 30 Sep 2025 15:44:04 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 30 Sep 2025 15:44:04 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 30 Sep 2025 15:44:04 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 30 Sep 2025 15:44:04 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 30 Sep 2025 15:44:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b272c35630b7d133c1f5e9a6ce1237660d2d77f2ac9eb9f3e60514612f12ec4b`  
		Last Modified: Mon, 22 Sep 2025 12:55:02 GMT  
		Size: 6.0 MB (5967917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d36feaa4b03a005a628052472c2233b0e31b1e544907db98efa5438e57b38e`  
		Last Modified: Wed, 08 Oct 2025 22:51:22 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:07430f24301701dbd1f4fa880f36a684281796cbf528965370f590e355c51b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2af80a79db21765de40b16adb89ae5adaad4eccd3698a99247ee3687b622a2f`

```dockerfile
```

-	Layers:
	-	`sha256:7197393d41541afdbccfb8a72d28f243b1d95b59d7e6c90f834e6297cdf78a96`  
		Last Modified: Wed, 08 Oct 2025 23:56:31 GMT  
		Size: 10.7 KB (10650 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:a72fb58fbf3ab27aad7639b9adb92207e4dec5210c83c5fb3f180808337d833d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6015640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6d57b963bc1b9dec9ade0c28b72ea67c82bc3167a529d44b3e41d23c595fe3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Sep 2025 12:53:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Sep 2025 12:53:23 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Sep 2025 12:53:23 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Sep 2025 12:53:23 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Sep 2025 12:53:23 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Sep 2025 12:53:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8da1665837c65551f19d52d35a7d28f01641553a8e18290e1a862967e9e22164`  
		Last Modified: Mon, 22 Sep 2025 20:39:59 GMT  
		Size: 6.0 MB (6015132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1ae75dc4352bd00646f340033ad540c47e41e90b9921f2806283e8baac67db`  
		Last Modified: Mon, 22 Sep 2025 20:39:24 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:6e591c916f3a8b03b2a2ae7779edce2888ded185cc13e123dd962e8969ed3140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8d0bf2d527cc4bba8edbc050f101fe863656498bd62fc12963060fa26d4e07`

```dockerfile
```

-	Layers:
	-	`sha256:a213b2c336ab8532e6f70e13e1861cac038960ef2baf5f4a6d82f347f1b54548`  
		Last Modified: Mon, 22 Sep 2025 20:56:46 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:a760ef3f4e005f90f1631c56148d1dbead64e6480b5fed083486a3dd457037b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6390563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78d894926f0275b20d1706181ed568374e958597923d8484f5910d16aba5ffcf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Sep 2025 12:53:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Sep 2025 12:53:23 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Sep 2025 12:53:23 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Sep 2025 12:53:23 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Sep 2025 12:53:23 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Sep 2025 12:53:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:90967c856d95f14cab3e9574b1a31898d63045102f8c2945dd81faecad959d89`  
		Last Modified: Mon, 22 Sep 2025 20:39:59 GMT  
		Size: 6.4 MB (6390055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4415798d4caa44059722e6ab52e5f183a6d3de50c92aa95621bbaa0b42934447`  
		Last Modified: Mon, 22 Sep 2025 20:39:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:1fad27a5cf516434c0c2fdd47e5f6066c5488a8b0b8141d82daf44090c878887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb2b2c7628309a69acfcfc0d741156c169ff47d96cece8ff10b951c49ac7731f`

```dockerfile
```

-	Layers:
	-	`sha256:6ab76f6d94ebe0152b5d00cefa9ada89ec8b90aaba494b30ae517f689eaf02c4`  
		Last Modified: Mon, 22 Sep 2025 20:56:49 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json
