<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.21`](#nats2-alpine321)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2.10`](#nats210)
-	[`nats:2.10-alpine`](#nats210-alpine)
-	[`nats:2.10-alpine3.21`](#nats210-alpine321)
-	[`nats:2.10-linux`](#nats210-linux)
-	[`nats:2.10-nanoserver`](#nats210-nanoserver)
-	[`nats:2.10-nanoserver-1809`](#nats210-nanoserver-1809)
-	[`nats:2.10-scratch`](#nats210-scratch)
-	[`nats:2.10-windowsservercore`](#nats210-windowsservercore)
-	[`nats:2.10-windowsservercore-1809`](#nats210-windowsservercore-1809)
-	[`nats:2.10.23`](#nats21023)
-	[`nats:2.10.23-alpine`](#nats21023-alpine)
-	[`nats:2.10.23-alpine3.21`](#nats21023-alpine321)
-	[`nats:2.10.23-linux`](#nats21023-linux)
-	[`nats:2.10.23-nanoserver`](#nats21023-nanoserver)
-	[`nats:2.10.23-nanoserver-1809`](#nats21023-nanoserver-1809)
-	[`nats:2.10.23-scratch`](#nats21023-scratch)
-	[`nats:2.10.23-windowsservercore`](#nats21023-windowsservercore)
-	[`nats:2.10.23-windowsservercore-1809`](#nats21023-windowsservercore-1809)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.21`](#natsalpine321)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)

## `nats:2`

```console
$ docker pull nats@sha256:d15749dc10d8e67b55f496551ca3794b2f131556342b313eb3e6115ec75f6fb3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
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
	-	windows version 10.0.17763.6532; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:26b0ee1a95285aedae137aefb953701d9da1dfffcf7818eb3aeb536c4373892f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9321c727224d6919153399a2554913ee3ea75615c40faf0b0b61719fd4cba18f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc7b6eeb42db27589fb02b7af7648621b4230b391664f1cabca731c0cb74c6c0`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.7 MB (5748809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648a1fe081b19052a39d36fde23ff89c48a0b60bddc52cdf58474ed9b7e16ab4`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:92b63acf1eb46cb3ce90a6406fcf9cf3214ba330e4dacef512280529a04870ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd7260fa709b7a3bb731d03f1fc89313f81c37eaacc9a95aef394dde1aa26ae`

```dockerfile
```

-	Layers:
	-	`sha256:eb1f99c4d9cf8c2d861e264c9ba0cdb9161bb70c2764c955ab1f90310af1f472`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:ed0d3d3f325c395d64fe3cce644fcb8a85dd7f693321155adc742f9a4558a524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5414498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb43c0fb21e266dce12015b728c78e144c79b548aa91729dffae13470e0d9297`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:359939d6b9b0e79cd20ca9621811c48e03c3d4a5b7af0a099486d520bf5d7b5f`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.4 MB (5413989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f789fb3e9d2d0ff4362d663dece6c6656816327c3c477f706bb39361ec1cd75`  
		Last Modified: Tue, 12 Nov 2024 15:37:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:6ed1504d0cb0d9a7e50ccb85fa202b5d8901dc4bc331ec9212598e39c7cb9708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35958b08d07b59577364ce756c66f53782d4b469b1eb5fa49f8e1d5b54cdca4`

```dockerfile
```

-	Layers:
	-	`sha256:4666424ba74b452fb83d3ee0779517652e5b5c382cd17ac41b3a6eed5fa553c9`  
		Last Modified: Tue, 12 Nov 2024 15:37:52 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:6e124d1272a57524b4ca6d20f067a1bcaaf0698436552c1e023098e8d86f3ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5402382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48a99f0a97426e5e74f3a25a607b2c16d9a4521a32a2ba12fa6fdd0202e4bf5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d05d846e8109608ff47e05c22bb31057b6b6430dcabb8110890869d111bd1b9e`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.4 MB (5401872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2f51350cd72f7f51dbac3739d56b990a14dbbf86618c4893c441ddc4b1bb8c`  
		Last Modified: Wed, 13 Nov 2024 06:50:55 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:8961a748bcb9e725a669f8fa2f9feb42d333982353b703fc2ab7d1dcc75672df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f520b399deef237b5cb2d8124b151ec2c5226e54324dd079da79164fb174dba`

```dockerfile
```

-	Layers:
	-	`sha256:1eee6a8956b4ad976df210a755d0ef0e99d56f92ba24d749b7da0611fad96580`  
		Last Modified: Wed, 13 Nov 2024 06:50:55 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a472fd5123d4894808a5300ae620b1fc75173683a27bef46da8f72cffc933c98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5311420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b2641c24dab528ab7f50965ba60bf552fd0741d08bce6d7eb119bdb14c2eb9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:38a1a08cf356fa2c344f9efdd2f487176ba47d86dbe408ea24116528e7638b79`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.3 MB (5310912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f500aab43d6d7fb9af41817fd3e6d15af8d2cea39f195b594bb2aaf7ea3f8a3e`  
		Last Modified: Wed, 13 Nov 2024 01:53:01 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:28b2143fc08c4b9fa3086b9adbeb584e61f0fd522723dab3544ba1cf8d69f896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b61c129357d5acdec05b9878360c584d3e152bff6203d60fb73bba1d793c8f`

```dockerfile
```

-	Layers:
	-	`sha256:4292e75d9c32bf0ba80c2339d71516e065e70a4058f12e0d895837e96fa29963`  
		Last Modified: Wed, 13 Nov 2024 01:53:01 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; ppc64le

```console
$ docker pull nats@sha256:bfc123cdde6254307ee92ec40bfec41601825fb47a75326b4360f44bab372a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe22c4f1bea64db8b0f24a64002aa2061b73145c74e4218b813d0639491ea37`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:76bf2b5924879fa33a4c81c16fab61afb5d237715cb64ef9e8847f5b8cd91151`  
		Last Modified: Thu, 17 Oct 2024 18:09:44 GMT  
		Size: 5.3 MB (5279091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22806de38895554cf572cdc72c340ce1c2a1e339ea920a8fd272f6908805d555`  
		Last Modified: Tue, 12 Nov 2024 15:01:33 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:c68e4834537eedd18677a7ba9c608218c21721b078d08969c0d9c47a48e5a2bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6620d942923f41e16c63215620c4590dade6c160c8b3464748128fc3f4fe9f1`

```dockerfile
```

-	Layers:
	-	`sha256:f936acbf9b3ac4e546df2f3f5b7c04867dfd20bc3b0efd62c5b655a66d588f46`  
		Last Modified: Tue, 12 Nov 2024 15:01:33 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:860ac3f0cce933e2518b5dfad7e4ceb5d0a65e5e4958848ea12f0e2cf6262e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b1957d328a071a836284d4b15fee34cc4d49960896e4f141a5d8ff677d654e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fffb3288c2f56b83007e69c7219ef513ffc8b9f7f218885669a4d81f7aea10c7`  
		Last Modified: Thu, 17 Oct 2024 18:09:45 GMT  
		Size: 5.6 MB (5603688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2fd1adb449a2e37ee7766e0822200ce9fef4742f0a63f4271d9db4b8e2f3f1`  
		Last Modified: Tue, 12 Nov 2024 22:35:30 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:0f6e8d82de7f4a5a2d5fc517757ceaf8a2a1411abfc8fdc89d44e7a32f7c1ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67bf5d4378b516209f4da80c21451bb69cbb934cf3b8d37e72dfbab1a5bb6c44`

```dockerfile
```

-	Layers:
	-	`sha256:236407df6864bbf886cc676be754b255160b1a1aece15f8331b5062b41bc981e`  
		Last Modified: Tue, 12 Nov 2024 22:35:30 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:af099d0ad09f68427f6716cbe03227c5409000f9021c92a4981a6099e9901dc7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161090154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e23925b656567c9ef8ee2bc478e0ada3269421cc962f905108b7ac70bfc5d2f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Thu, 14 Nov 2024 21:26:06 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 14 Nov 2024 21:26:11 GMT
RUN cmd /S /C #(nop) COPY file:6efa011ff84014d148ada9315a3292149a71c3daa1b536499f2b43a2daee2d50 in C:\nats-server.exe 
# Thu, 14 Nov 2024 21:26:12 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Nov 2024 21:26:12 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 14 Nov 2024 21:26:13 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Nov 2024 21:26:14 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077c935cc00e1acf8d3769c81d23f3134507c1149593f2af1de160f98fd769e3`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb87536f0d2cb71d86892dcf0a7036c92d682cdf7e3a8dadda31d9569a62118`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 5.9 MB (5870083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929a1f4fa9be7e6e28a451ae8e437938d70bb70ab75539f175ac46be518d2292`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d64f781d33814e56a5a3e633b6778e34fb06d03ee0cf92a7b1931ffea43af5`  
		Last Modified: Thu, 14 Nov 2024 21:26:16 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f881ff7235bc92d60a608d0336719df84a7f2a45c17ef58277f678e69e3acb1b`  
		Last Modified: Thu, 14 Nov 2024 21:26:16 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d5e5b49ab6c4788712962e67498e176b4fdb803f692b97a96580ca87f612c`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:28de350897b589b46cbe9be25abd075eaad0faeb45ab4b1c832d1fa0dcf28d6d
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

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:1fd834581735b304465d440d706f668b245fa15c90864a8110d0069628504799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10017410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69bad2eb78b7ad191ae578a8cd1a90bb014cd770b959fdf75228696af9e957b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3eb8f37ad7a3d0e0d42022d3b399dbeb45f39b9a36dd95f9c74eb3ee4ff505`  
		Last Modified: Tue, 10 Dec 2024 23:27:27 GMT  
		Size: 6.4 MB (6371998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d30e571e9a33b90d53adc364b75dc4175a04f59de9d03895a30448068789fd`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64e4621359f08beab60eaf8e077f6f6ab0cec1ab6c999d1fdb4b35235662973`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:205d307881aedf2bd51cd9499b2e7cab47ada6b75a95df123216ad185b195a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9195c0eaed762824d5c53e56fe0b79a7d0d6375197aea07ffe383a513bb9a998`

```dockerfile
```

-	Layers:
	-	`sha256:069960ecffcdfc8e80d9352cfbe93b35fda077faf6c558950c05b3be76d07796`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:3569b3c6c6049c65c064d2c1638f58c6373d9779bfbafa529c82b117df449f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9387859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78fb87af3390f4d569e90248e5ef868c71ea224696608d9676420a21f08204f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d491d6ae32f791b6c6ee444da2433c3fe5f68f95a28a063e08fba789ebeb3f1`  
		Last Modified: Tue, 10 Dec 2024 23:27:13 GMT  
		Size: 6.0 MB (6019710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865e30e55f10109ec4fa649ff5598bb63785974f48e3467909963032f1b75bf3`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e27652e6cdf62ea6391042bda7e59583d83826301e119078799dc7674d5f916`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5c9032bdc8ef63d822723910e03076cf5c904847843dde7aa3597eb73c844ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4723e93aa61b1d00a73afea3fa2d282ca9b9cfbf288b20c9edb846ddc14746`

```dockerfile
```

-	Layers:
	-	`sha256:e07ee39720e7781ee4b9ccfe13bf58df6e7045efc1ed482c9f6a811ceb5c4cb0`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a0825f66cb5b9d7837459726ec6ca63a60b3888e8b67c655c7bd4c0ba05448cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9108253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9dd517c3a03af5824c23a81cedeed2598c4db1f301b3bc2e9bc40f4ab1bd618`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c84334747ecb5ce1375e80f91f5c140846eb6d7d51f9f6e6706641e1534c47`  
		Last Modified: Tue, 10 Dec 2024 23:27:11 GMT  
		Size: 6.0 MB (6007249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8010f8f3390c5e4323711c7f680070162d24e7fe3a14cf0e3d4670bd86647f9f`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573b54805f27aadae125876129ffbe488c10a85a15c36f50824d9ea4120537db`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6332c66401722e3837a6d186f7f9e1998a51350aa4b0af94507fbabb700ebb51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8a5df688f658118f4802867e4073818b174fd568574578a38138431bcbe412`

```dockerfile
```

-	Layers:
	-	`sha256:90edcaab6c14939090cda88a4bafbf0f09deddae7ca690ec3b1cda3e66db02a9`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:44905153cfe19be67e2baf248d1fe4a687aa2542e28efbff0f08f466e8749d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9912066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18b42869bfcbe5193535e39dc5571d303f0fcfd8c8fef4c6bb885ebe9b16b70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab592abba0f5f4ec119ae6d68f1206012d0485e97bb32949ec2a5bd04eb22f6`  
		Last Modified: Tue, 10 Dec 2024 23:27:05 GMT  
		Size: 5.9 MB (5917911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83961d61cdbd8298afd926b21e9e703be42edad95c17d626d5b2c8f8bdfafca`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403efcdcd91f4b94baeb36d579d722af0241889ee36afa8b92229b2c6eb937b4`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a25a621ca70ce2b0b97e30ce8ff0dbaed26cdf192d3a9f357bee0ee044c610d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850950126604011113cf97360a1b385355861ecabbe661483a1173cd8dd61172`

```dockerfile
```

-	Layers:
	-	`sha256:92f99c76a992a8785e402afdc8c8fee96331b60410b4a73baacc424b5d4ef722`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:d23003b22072b07cea7c57403d30519c9974445420181d8e174fbfa45fa533ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b0b23cf06fe3a7a78cbf9050f6de38b3cbd86fd9eadd9aa0b576d10af31480`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aaaa26dccaea10b5b83d01ed56f7a196c902179c89f7b031693a66884d17aef`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 5.7 MB (5738932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd34510b2845266284f593caae986bea90464fb438d79811c16c21afc268db9`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2beb0025099f5180f9671beb5f58c8b9fb8950f5971472ca2aded6d8c086dfcc`  
		Last Modified: Tue, 12 Nov 2024 03:03:02 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6ff0dd9b59f440e98ec6d6043cae3c81909695d9cf72e4f75ee2729e8104db86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72e08b6ff60c9977edbbe63a98b79f532617da8c1b3435d620244dd54347bea`

```dockerfile
```

-	Layers:
	-	`sha256:5f8a5a969359fee4a9f6bfec8cf77271b3a9243079c36ba7fbda1fadd5e0130c`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:d62285e97415380d73c75ff154d35fa1c6d6bec23a71995a671e665405d855b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9687191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658e5ca2d2437afce8173f52960e6280cfc673cd68edd78c9b60d8e50f94624b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f889b72b6e6f2f7a8f55853722d58f9f51fb766899e07465539676a22f0ca84`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 6.2 MB (6216702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995a4bc6424d4d94211f245dfd6f8f7975eea36b074521a866fbb75000ae79cd`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2990cf750e1e6ae965cb5ee3aa09fb5555f8709d7b9fd091ff70f124dd53a69d`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ef1002190acf6bcefe4da93459355df9b9bd492b52bf5895f710fadb82698c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bbee94701029b1f45fcbe9dbe8783e933466d45dd6eeefdb23d66cbb64483b5`

```dockerfile
```

-	Layers:
	-	`sha256:8c627f5f6e115176dd03af0a018e19fad71b8bb00277a4792730d383bd1e9868`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-alpine3.21`

```console
$ docker pull nats@sha256:87ed4c1ce118ac91e10e8b917c75085959d008a69219f32a0ddd3f31619b1adf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:1fd834581735b304465d440d706f668b245fa15c90864a8110d0069628504799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10017410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69bad2eb78b7ad191ae578a8cd1a90bb014cd770b959fdf75228696af9e957b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3eb8f37ad7a3d0e0d42022d3b399dbeb45f39b9a36dd95f9c74eb3ee4ff505`  
		Last Modified: Tue, 10 Dec 2024 23:27:27 GMT  
		Size: 6.4 MB (6371998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d30e571e9a33b90d53adc364b75dc4175a04f59de9d03895a30448068789fd`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64e4621359f08beab60eaf8e077f6f6ab0cec1ab6c999d1fdb4b35235662973`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:205d307881aedf2bd51cd9499b2e7cab47ada6b75a95df123216ad185b195a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9195c0eaed762824d5c53e56fe0b79a7d0d6375197aea07ffe383a513bb9a998`

```dockerfile
```

-	Layers:
	-	`sha256:069960ecffcdfc8e80d9352cfbe93b35fda077faf6c558950c05b3be76d07796`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:3569b3c6c6049c65c064d2c1638f58c6373d9779bfbafa529c82b117df449f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9387859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78fb87af3390f4d569e90248e5ef868c71ea224696608d9676420a21f08204f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d491d6ae32f791b6c6ee444da2433c3fe5f68f95a28a063e08fba789ebeb3f1`  
		Last Modified: Tue, 10 Dec 2024 23:27:13 GMT  
		Size: 6.0 MB (6019710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865e30e55f10109ec4fa649ff5598bb63785974f48e3467909963032f1b75bf3`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e27652e6cdf62ea6391042bda7e59583d83826301e119078799dc7674d5f916`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:5c9032bdc8ef63d822723910e03076cf5c904847843dde7aa3597eb73c844ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4723e93aa61b1d00a73afea3fa2d282ca9b9cfbf288b20c9edb846ddc14746`

```dockerfile
```

-	Layers:
	-	`sha256:e07ee39720e7781ee4b9ccfe13bf58df6e7045efc1ed482c9f6a811ceb5c4cb0`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:a0825f66cb5b9d7837459726ec6ca63a60b3888e8b67c655c7bd4c0ba05448cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9108253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9dd517c3a03af5824c23a81cedeed2598c4db1f301b3bc2e9bc40f4ab1bd618`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c84334747ecb5ce1375e80f91f5c140846eb6d7d51f9f6e6706641e1534c47`  
		Last Modified: Tue, 10 Dec 2024 23:27:11 GMT  
		Size: 6.0 MB (6007249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8010f8f3390c5e4323711c7f680070162d24e7fe3a14cf0e3d4670bd86647f9f`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573b54805f27aadae125876129ffbe488c10a85a15c36f50824d9ea4120537db`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:6332c66401722e3837a6d186f7f9e1998a51350aa4b0af94507fbabb700ebb51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8a5df688f658118f4802867e4073818b174fd568574578a38138431bcbe412`

```dockerfile
```

-	Layers:
	-	`sha256:90edcaab6c14939090cda88a4bafbf0f09deddae7ca690ec3b1cda3e66db02a9`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:44905153cfe19be67e2baf248d1fe4a687aa2542e28efbff0f08f466e8749d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9912066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18b42869bfcbe5193535e39dc5571d303f0fcfd8c8fef4c6bb885ebe9b16b70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab592abba0f5f4ec119ae6d68f1206012d0485e97bb32949ec2a5bd04eb22f6`  
		Last Modified: Tue, 10 Dec 2024 23:27:05 GMT  
		Size: 5.9 MB (5917911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83961d61cdbd8298afd926b21e9e703be42edad95c17d626d5b2c8f8bdfafca`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403efcdcd91f4b94baeb36d579d722af0241889ee36afa8b92229b2c6eb937b4`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:a25a621ca70ce2b0b97e30ce8ff0dbaed26cdf192d3a9f357bee0ee044c610d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850950126604011113cf97360a1b385355861ecabbe661483a1173cd8dd61172`

```dockerfile
```

-	Layers:
	-	`sha256:92f99c76a992a8785e402afdc8c8fee96331b60410b4a73baacc424b5d4ef722`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:d62285e97415380d73c75ff154d35fa1c6d6bec23a71995a671e665405d855b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9687191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658e5ca2d2437afce8173f52960e6280cfc673cd68edd78c9b60d8e50f94624b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f889b72b6e6f2f7a8f55853722d58f9f51fb766899e07465539676a22f0ca84`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 6.2 MB (6216702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995a4bc6424d4d94211f245dfd6f8f7975eea36b074521a866fbb75000ae79cd`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2990cf750e1e6ae965cb5ee3aa09fb5555f8709d7b9fd091ff70f124dd53a69d`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:ef1002190acf6bcefe4da93459355df9b9bd492b52bf5895f710fadb82698c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bbee94701029b1f45fcbe9dbe8783e933466d45dd6eeefdb23d66cbb64483b5`

```dockerfile
```

-	Layers:
	-	`sha256:8c627f5f6e115176dd03af0a018e19fad71b8bb00277a4792730d383bd1e9868`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-linux`

```console
$ docker pull nats@sha256:23638865a8c200681a3a58ee86cd9c5776bbc7499f5525ce9c9baae4d4970d2a
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

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:26b0ee1a95285aedae137aefb953701d9da1dfffcf7818eb3aeb536c4373892f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9321c727224d6919153399a2554913ee3ea75615c40faf0b0b61719fd4cba18f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc7b6eeb42db27589fb02b7af7648621b4230b391664f1cabca731c0cb74c6c0`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.7 MB (5748809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648a1fe081b19052a39d36fde23ff89c48a0b60bddc52cdf58474ed9b7e16ab4`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:92b63acf1eb46cb3ce90a6406fcf9cf3214ba330e4dacef512280529a04870ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd7260fa709b7a3bb731d03f1fc89313f81c37eaacc9a95aef394dde1aa26ae`

```dockerfile
```

-	Layers:
	-	`sha256:eb1f99c4d9cf8c2d861e264c9ba0cdb9161bb70c2764c955ab1f90310af1f472`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:ed0d3d3f325c395d64fe3cce644fcb8a85dd7f693321155adc742f9a4558a524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5414498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb43c0fb21e266dce12015b728c78e144c79b548aa91729dffae13470e0d9297`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:359939d6b9b0e79cd20ca9621811c48e03c3d4a5b7af0a099486d520bf5d7b5f`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.4 MB (5413989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f789fb3e9d2d0ff4362d663dece6c6656816327c3c477f706bb39361ec1cd75`  
		Last Modified: Tue, 12 Nov 2024 15:37:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:6ed1504d0cb0d9a7e50ccb85fa202b5d8901dc4bc331ec9212598e39c7cb9708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35958b08d07b59577364ce756c66f53782d4b469b1eb5fa49f8e1d5b54cdca4`

```dockerfile
```

-	Layers:
	-	`sha256:4666424ba74b452fb83d3ee0779517652e5b5c382cd17ac41b3a6eed5fa553c9`  
		Last Modified: Tue, 12 Nov 2024 15:37:52 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:6e124d1272a57524b4ca6d20f067a1bcaaf0698436552c1e023098e8d86f3ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5402382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48a99f0a97426e5e74f3a25a607b2c16d9a4521a32a2ba12fa6fdd0202e4bf5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d05d846e8109608ff47e05c22bb31057b6b6430dcabb8110890869d111bd1b9e`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.4 MB (5401872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2f51350cd72f7f51dbac3739d56b990a14dbbf86618c4893c441ddc4b1bb8c`  
		Last Modified: Wed, 13 Nov 2024 06:50:55 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:8961a748bcb9e725a669f8fa2f9feb42d333982353b703fc2ab7d1dcc75672df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f520b399deef237b5cb2d8124b151ec2c5226e54324dd079da79164fb174dba`

```dockerfile
```

-	Layers:
	-	`sha256:1eee6a8956b4ad976df210a755d0ef0e99d56f92ba24d749b7da0611fad96580`  
		Last Modified: Wed, 13 Nov 2024 06:50:55 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a472fd5123d4894808a5300ae620b1fc75173683a27bef46da8f72cffc933c98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5311420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b2641c24dab528ab7f50965ba60bf552fd0741d08bce6d7eb119bdb14c2eb9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:38a1a08cf356fa2c344f9efdd2f487176ba47d86dbe408ea24116528e7638b79`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.3 MB (5310912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f500aab43d6d7fb9af41817fd3e6d15af8d2cea39f195b594bb2aaf7ea3f8a3e`  
		Last Modified: Wed, 13 Nov 2024 01:53:01 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:28b2143fc08c4b9fa3086b9adbeb584e61f0fd522723dab3544ba1cf8d69f896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b61c129357d5acdec05b9878360c584d3e152bff6203d60fb73bba1d793c8f`

```dockerfile
```

-	Layers:
	-	`sha256:4292e75d9c32bf0ba80c2339d71516e065e70a4058f12e0d895837e96fa29963`  
		Last Modified: Wed, 13 Nov 2024 01:53:01 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:bfc123cdde6254307ee92ec40bfec41601825fb47a75326b4360f44bab372a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe22c4f1bea64db8b0f24a64002aa2061b73145c74e4218b813d0639491ea37`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:76bf2b5924879fa33a4c81c16fab61afb5d237715cb64ef9e8847f5b8cd91151`  
		Last Modified: Thu, 17 Oct 2024 18:09:44 GMT  
		Size: 5.3 MB (5279091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22806de38895554cf572cdc72c340ce1c2a1e339ea920a8fd272f6908805d555`  
		Last Modified: Tue, 12 Nov 2024 15:01:33 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:c68e4834537eedd18677a7ba9c608218c21721b078d08969c0d9c47a48e5a2bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6620d942923f41e16c63215620c4590dade6c160c8b3464748128fc3f4fe9f1`

```dockerfile
```

-	Layers:
	-	`sha256:f936acbf9b3ac4e546df2f3f5b7c04867dfd20bc3b0efd62c5b655a66d588f46`  
		Last Modified: Tue, 12 Nov 2024 15:01:33 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:860ac3f0cce933e2518b5dfad7e4ceb5d0a65e5e4958848ea12f0e2cf6262e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b1957d328a071a836284d4b15fee34cc4d49960896e4f141a5d8ff677d654e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fffb3288c2f56b83007e69c7219ef513ffc8b9f7f218885669a4d81f7aea10c7`  
		Last Modified: Thu, 17 Oct 2024 18:09:45 GMT  
		Size: 5.6 MB (5603688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2fd1adb449a2e37ee7766e0822200ce9fef4742f0a63f4271d9db4b8e2f3f1`  
		Last Modified: Tue, 12 Nov 2024 22:35:30 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:0f6e8d82de7f4a5a2d5fc517757ceaf8a2a1411abfc8fdc89d44e7a32f7c1ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67bf5d4378b516209f4da80c21451bb69cbb934cf3b8d37e72dfbab1a5bb6c44`

```dockerfile
```

-	Layers:
	-	`sha256:236407df6864bbf886cc676be754b255160b1a1aece15f8331b5062b41bc981e`  
		Last Modified: Tue, 12 Nov 2024 22:35:30 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:070f9e269bf92f0bedac63b5a0f269f7520ad54e071f7953b5c35621160ad025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:af099d0ad09f68427f6716cbe03227c5409000f9021c92a4981a6099e9901dc7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161090154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e23925b656567c9ef8ee2bc478e0ada3269421cc962f905108b7ac70bfc5d2f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Thu, 14 Nov 2024 21:26:06 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 14 Nov 2024 21:26:11 GMT
RUN cmd /S /C #(nop) COPY file:6efa011ff84014d148ada9315a3292149a71c3daa1b536499f2b43a2daee2d50 in C:\nats-server.exe 
# Thu, 14 Nov 2024 21:26:12 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Nov 2024 21:26:12 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 14 Nov 2024 21:26:13 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Nov 2024 21:26:14 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077c935cc00e1acf8d3769c81d23f3134507c1149593f2af1de160f98fd769e3`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb87536f0d2cb71d86892dcf0a7036c92d682cdf7e3a8dadda31d9569a62118`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 5.9 MB (5870083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929a1f4fa9be7e6e28a451ae8e437938d70bb70ab75539f175ac46be518d2292`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d64f781d33814e56a5a3e633b6778e34fb06d03ee0cf92a7b1931ffea43af5`  
		Last Modified: Thu, 14 Nov 2024 21:26:16 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f881ff7235bc92d60a608d0336719df84a7f2a45c17ef58277f678e69e3acb1b`  
		Last Modified: Thu, 14 Nov 2024 21:26:16 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d5e5b49ab6c4788712962e67498e176b4fdb803f692b97a96580ca87f612c`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:070f9e269bf92f0bedac63b5a0f269f7520ad54e071f7953b5c35621160ad025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:af099d0ad09f68427f6716cbe03227c5409000f9021c92a4981a6099e9901dc7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161090154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e23925b656567c9ef8ee2bc478e0ada3269421cc962f905108b7ac70bfc5d2f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Thu, 14 Nov 2024 21:26:06 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 14 Nov 2024 21:26:11 GMT
RUN cmd /S /C #(nop) COPY file:6efa011ff84014d148ada9315a3292149a71c3daa1b536499f2b43a2daee2d50 in C:\nats-server.exe 
# Thu, 14 Nov 2024 21:26:12 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Nov 2024 21:26:12 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 14 Nov 2024 21:26:13 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Nov 2024 21:26:14 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077c935cc00e1acf8d3769c81d23f3134507c1149593f2af1de160f98fd769e3`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb87536f0d2cb71d86892dcf0a7036c92d682cdf7e3a8dadda31d9569a62118`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 5.9 MB (5870083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929a1f4fa9be7e6e28a451ae8e437938d70bb70ab75539f175ac46be518d2292`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d64f781d33814e56a5a3e633b6778e34fb06d03ee0cf92a7b1931ffea43af5`  
		Last Modified: Thu, 14 Nov 2024 21:26:16 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f881ff7235bc92d60a608d0336719df84a7f2a45c17ef58277f678e69e3acb1b`  
		Last Modified: Thu, 14 Nov 2024 21:26:16 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d5e5b49ab6c4788712962e67498e176b4fdb803f692b97a96580ca87f612c`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:23638865a8c200681a3a58ee86cd9c5776bbc7499f5525ce9c9baae4d4970d2a
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

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:26b0ee1a95285aedae137aefb953701d9da1dfffcf7818eb3aeb536c4373892f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9321c727224d6919153399a2554913ee3ea75615c40faf0b0b61719fd4cba18f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc7b6eeb42db27589fb02b7af7648621b4230b391664f1cabca731c0cb74c6c0`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.7 MB (5748809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648a1fe081b19052a39d36fde23ff89c48a0b60bddc52cdf58474ed9b7e16ab4`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:92b63acf1eb46cb3ce90a6406fcf9cf3214ba330e4dacef512280529a04870ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd7260fa709b7a3bb731d03f1fc89313f81c37eaacc9a95aef394dde1aa26ae`

```dockerfile
```

-	Layers:
	-	`sha256:eb1f99c4d9cf8c2d861e264c9ba0cdb9161bb70c2764c955ab1f90310af1f472`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:ed0d3d3f325c395d64fe3cce644fcb8a85dd7f693321155adc742f9a4558a524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5414498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb43c0fb21e266dce12015b728c78e144c79b548aa91729dffae13470e0d9297`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:359939d6b9b0e79cd20ca9621811c48e03c3d4a5b7af0a099486d520bf5d7b5f`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.4 MB (5413989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f789fb3e9d2d0ff4362d663dece6c6656816327c3c477f706bb39361ec1cd75`  
		Last Modified: Tue, 12 Nov 2024 15:37:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:6ed1504d0cb0d9a7e50ccb85fa202b5d8901dc4bc331ec9212598e39c7cb9708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35958b08d07b59577364ce756c66f53782d4b469b1eb5fa49f8e1d5b54cdca4`

```dockerfile
```

-	Layers:
	-	`sha256:4666424ba74b452fb83d3ee0779517652e5b5c382cd17ac41b3a6eed5fa553c9`  
		Last Modified: Tue, 12 Nov 2024 15:37:52 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:6e124d1272a57524b4ca6d20f067a1bcaaf0698436552c1e023098e8d86f3ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5402382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48a99f0a97426e5e74f3a25a607b2c16d9a4521a32a2ba12fa6fdd0202e4bf5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d05d846e8109608ff47e05c22bb31057b6b6430dcabb8110890869d111bd1b9e`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.4 MB (5401872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2f51350cd72f7f51dbac3739d56b990a14dbbf86618c4893c441ddc4b1bb8c`  
		Last Modified: Wed, 13 Nov 2024 06:50:55 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:8961a748bcb9e725a669f8fa2f9feb42d333982353b703fc2ab7d1dcc75672df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f520b399deef237b5cb2d8124b151ec2c5226e54324dd079da79164fb174dba`

```dockerfile
```

-	Layers:
	-	`sha256:1eee6a8956b4ad976df210a755d0ef0e99d56f92ba24d749b7da0611fad96580`  
		Last Modified: Wed, 13 Nov 2024 06:50:55 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a472fd5123d4894808a5300ae620b1fc75173683a27bef46da8f72cffc933c98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5311420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b2641c24dab528ab7f50965ba60bf552fd0741d08bce6d7eb119bdb14c2eb9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:38a1a08cf356fa2c344f9efdd2f487176ba47d86dbe408ea24116528e7638b79`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.3 MB (5310912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f500aab43d6d7fb9af41817fd3e6d15af8d2cea39f195b594bb2aaf7ea3f8a3e`  
		Last Modified: Wed, 13 Nov 2024 01:53:01 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:28b2143fc08c4b9fa3086b9adbeb584e61f0fd522723dab3544ba1cf8d69f896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b61c129357d5acdec05b9878360c584d3e152bff6203d60fb73bba1d793c8f`

```dockerfile
```

-	Layers:
	-	`sha256:4292e75d9c32bf0ba80c2339d71516e065e70a4058f12e0d895837e96fa29963`  
		Last Modified: Wed, 13 Nov 2024 01:53:01 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:bfc123cdde6254307ee92ec40bfec41601825fb47a75326b4360f44bab372a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe22c4f1bea64db8b0f24a64002aa2061b73145c74e4218b813d0639491ea37`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:76bf2b5924879fa33a4c81c16fab61afb5d237715cb64ef9e8847f5b8cd91151`  
		Last Modified: Thu, 17 Oct 2024 18:09:44 GMT  
		Size: 5.3 MB (5279091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22806de38895554cf572cdc72c340ce1c2a1e339ea920a8fd272f6908805d555`  
		Last Modified: Tue, 12 Nov 2024 15:01:33 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:c68e4834537eedd18677a7ba9c608218c21721b078d08969c0d9c47a48e5a2bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6620d942923f41e16c63215620c4590dade6c160c8b3464748128fc3f4fe9f1`

```dockerfile
```

-	Layers:
	-	`sha256:f936acbf9b3ac4e546df2f3f5b7c04867dfd20bc3b0efd62c5b655a66d588f46`  
		Last Modified: Tue, 12 Nov 2024 15:01:33 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:860ac3f0cce933e2518b5dfad7e4ceb5d0a65e5e4958848ea12f0e2cf6262e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b1957d328a071a836284d4b15fee34cc4d49960896e4f141a5d8ff677d654e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fffb3288c2f56b83007e69c7219ef513ffc8b9f7f218885669a4d81f7aea10c7`  
		Last Modified: Thu, 17 Oct 2024 18:09:45 GMT  
		Size: 5.6 MB (5603688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2fd1adb449a2e37ee7766e0822200ce9fef4742f0a63f4271d9db4b8e2f3f1`  
		Last Modified: Tue, 12 Nov 2024 22:35:30 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:0f6e8d82de7f4a5a2d5fc517757ceaf8a2a1411abfc8fdc89d44e7a32f7c1ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67bf5d4378b516209f4da80c21451bb69cbb934cf3b8d37e72dfbab1a5bb6c44`

```dockerfile
```

-	Layers:
	-	`sha256:236407df6864bbf886cc676be754b255160b1a1aece15f8331b5062b41bc981e`  
		Last Modified: Tue, 12 Nov 2024 22:35:30 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:43fbcf8dfa35b4760178e0b4e16c2474d68f1ab3128b980817133057582d7e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:d8404f289d887ce07c6ec8c2ed3f2512727f6d6d33791e6f0d607f03a7bb99d0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2017532110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91991216a6a1544d8f469907d8e4e7e7aeb83722aa7f22591fb24566360cc0ab`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Tue, 10 Dec 2024 23:27:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Dec 2024 23:27:31 GMT
ENV NATS_DOCKERIZED=1
# Tue, 10 Dec 2024 23:27:32 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 23:27:32 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.23/nats-server-v2.10.23-windows-amd64.zip
# Tue, 10 Dec 2024 23:27:33 GMT
ENV NATS_SERVER_SHASUM=4ec39c0df08823a062dcdaac23ccf7ee56e76ccc27b69134f3e9b1549bc0f305
# Tue, 10 Dec 2024 23:28:50 GMT
RUN Set-PSDebug -Trace 2
# Tue, 10 Dec 2024 23:29:14 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 10 Dec 2024 23:29:14 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 10 Dec 2024 23:29:15 GMT
EXPOSE 4222 6222 8222
# Tue, 10 Dec 2024 23:29:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Dec 2024 23:29:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05963517ca3d5c411c11e9cf4ac529f3affa194a7f0914374d3b98008e19fcd`  
		Last Modified: Tue, 10 Dec 2024 23:29:20 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d8577eb6f25bb0f27f3d64f76584102e62ec7d909b34960f3f37f832653a0e`  
		Last Modified: Tue, 10 Dec 2024 23:29:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d70b39f16077baba91f50f30b3e69fbb08e38919da455c6ab5aad8d102b0a4`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231308f503d04392a55f1811db0102c1873660ab3780d766220170f78845628d`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8454af0dc55c7414c29902b1ae692d77206dbf2d5e0329ea7f4d00b32e43981f`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae10fbf74e9db38c4b611d58d3aabebe4336ef55f067d024a5753990d8ee0c65`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 485.0 KB (485022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b00a4239ecfe83a559cd5f40ff7a390b535f2c4a718c1dfcb11fb36e643bc6`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 6.4 MB (6381052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293d2ecab9ac866fa0d9cd648139d9576b12e77960c11dd976d1e874a69074e3`  
		Last Modified: Tue, 10 Dec 2024 23:29:18 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcaf4545aa895aefcb8f088f2fada2e81ed4f5ea5070c634da65a3226c5f454d`  
		Last Modified: Tue, 10 Dec 2024 23:29:18 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be99fe33f983eb453fe8c100eb4bc03e6d17392e701deae38cf0dcb416b86635`  
		Last Modified: Tue, 10 Dec 2024 23:29:18 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ace41bfa487712fd128caaa0b1ddb268f5cc6f198c990a822fa0b9a55c0cee7`  
		Last Modified: Tue, 10 Dec 2024 23:29:18 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:43fbcf8dfa35b4760178e0b4e16c2474d68f1ab3128b980817133057582d7e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:d8404f289d887ce07c6ec8c2ed3f2512727f6d6d33791e6f0d607f03a7bb99d0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2017532110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91991216a6a1544d8f469907d8e4e7e7aeb83722aa7f22591fb24566360cc0ab`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Tue, 10 Dec 2024 23:27:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Dec 2024 23:27:31 GMT
ENV NATS_DOCKERIZED=1
# Tue, 10 Dec 2024 23:27:32 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 23:27:32 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.23/nats-server-v2.10.23-windows-amd64.zip
# Tue, 10 Dec 2024 23:27:33 GMT
ENV NATS_SERVER_SHASUM=4ec39c0df08823a062dcdaac23ccf7ee56e76ccc27b69134f3e9b1549bc0f305
# Tue, 10 Dec 2024 23:28:50 GMT
RUN Set-PSDebug -Trace 2
# Tue, 10 Dec 2024 23:29:14 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 10 Dec 2024 23:29:14 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 10 Dec 2024 23:29:15 GMT
EXPOSE 4222 6222 8222
# Tue, 10 Dec 2024 23:29:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Dec 2024 23:29:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05963517ca3d5c411c11e9cf4ac529f3affa194a7f0914374d3b98008e19fcd`  
		Last Modified: Tue, 10 Dec 2024 23:29:20 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d8577eb6f25bb0f27f3d64f76584102e62ec7d909b34960f3f37f832653a0e`  
		Last Modified: Tue, 10 Dec 2024 23:29:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d70b39f16077baba91f50f30b3e69fbb08e38919da455c6ab5aad8d102b0a4`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231308f503d04392a55f1811db0102c1873660ab3780d766220170f78845628d`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8454af0dc55c7414c29902b1ae692d77206dbf2d5e0329ea7f4d00b32e43981f`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae10fbf74e9db38c4b611d58d3aabebe4336ef55f067d024a5753990d8ee0c65`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 485.0 KB (485022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b00a4239ecfe83a559cd5f40ff7a390b535f2c4a718c1dfcb11fb36e643bc6`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 6.4 MB (6381052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293d2ecab9ac866fa0d9cd648139d9576b12e77960c11dd976d1e874a69074e3`  
		Last Modified: Tue, 10 Dec 2024 23:29:18 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcaf4545aa895aefcb8f088f2fada2e81ed4f5ea5070c634da65a3226c5f454d`  
		Last Modified: Tue, 10 Dec 2024 23:29:18 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be99fe33f983eb453fe8c100eb4bc03e6d17392e701deae38cf0dcb416b86635`  
		Last Modified: Tue, 10 Dec 2024 23:29:18 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ace41bfa487712fd128caaa0b1ddb268f5cc6f198c990a822fa0b9a55c0cee7`  
		Last Modified: Tue, 10 Dec 2024 23:29:18 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:d15749dc10d8e67b55f496551ca3794b2f131556342b313eb3e6115ec75f6fb3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
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
	-	windows version 10.0.17763.6532; amd64

### `nats:2.10` - linux; amd64

```console
$ docker pull nats@sha256:26b0ee1a95285aedae137aefb953701d9da1dfffcf7818eb3aeb536c4373892f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9321c727224d6919153399a2554913ee3ea75615c40faf0b0b61719fd4cba18f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc7b6eeb42db27589fb02b7af7648621b4230b391664f1cabca731c0cb74c6c0`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.7 MB (5748809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648a1fe081b19052a39d36fde23ff89c48a0b60bddc52cdf58474ed9b7e16ab4`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:92b63acf1eb46cb3ce90a6406fcf9cf3214ba330e4dacef512280529a04870ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd7260fa709b7a3bb731d03f1fc89313f81c37eaacc9a95aef394dde1aa26ae`

```dockerfile
```

-	Layers:
	-	`sha256:eb1f99c4d9cf8c2d861e264c9ba0cdb9161bb70c2764c955ab1f90310af1f472`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:ed0d3d3f325c395d64fe3cce644fcb8a85dd7f693321155adc742f9a4558a524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5414498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb43c0fb21e266dce12015b728c78e144c79b548aa91729dffae13470e0d9297`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:359939d6b9b0e79cd20ca9621811c48e03c3d4a5b7af0a099486d520bf5d7b5f`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.4 MB (5413989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f789fb3e9d2d0ff4362d663dece6c6656816327c3c477f706bb39361ec1cd75`  
		Last Modified: Tue, 12 Nov 2024 15:37:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:6ed1504d0cb0d9a7e50ccb85fa202b5d8901dc4bc331ec9212598e39c7cb9708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35958b08d07b59577364ce756c66f53782d4b469b1eb5fa49f8e1d5b54cdca4`

```dockerfile
```

-	Layers:
	-	`sha256:4666424ba74b452fb83d3ee0779517652e5b5c382cd17ac41b3a6eed5fa553c9`  
		Last Modified: Tue, 12 Nov 2024 15:37:52 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:6e124d1272a57524b4ca6d20f067a1bcaaf0698436552c1e023098e8d86f3ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5402382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48a99f0a97426e5e74f3a25a607b2c16d9a4521a32a2ba12fa6fdd0202e4bf5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d05d846e8109608ff47e05c22bb31057b6b6430dcabb8110890869d111bd1b9e`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.4 MB (5401872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2f51350cd72f7f51dbac3739d56b990a14dbbf86618c4893c441ddc4b1bb8c`  
		Last Modified: Wed, 13 Nov 2024 06:50:55 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:8961a748bcb9e725a669f8fa2f9feb42d333982353b703fc2ab7d1dcc75672df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f520b399deef237b5cb2d8124b151ec2c5226e54324dd079da79164fb174dba`

```dockerfile
```

-	Layers:
	-	`sha256:1eee6a8956b4ad976df210a755d0ef0e99d56f92ba24d749b7da0611fad96580`  
		Last Modified: Wed, 13 Nov 2024 06:50:55 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a472fd5123d4894808a5300ae620b1fc75173683a27bef46da8f72cffc933c98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5311420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b2641c24dab528ab7f50965ba60bf552fd0741d08bce6d7eb119bdb14c2eb9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:38a1a08cf356fa2c344f9efdd2f487176ba47d86dbe408ea24116528e7638b79`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.3 MB (5310912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f500aab43d6d7fb9af41817fd3e6d15af8d2cea39f195b594bb2aaf7ea3f8a3e`  
		Last Modified: Wed, 13 Nov 2024 01:53:01 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:28b2143fc08c4b9fa3086b9adbeb584e61f0fd522723dab3544ba1cf8d69f896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b61c129357d5acdec05b9878360c584d3e152bff6203d60fb73bba1d793c8f`

```dockerfile
```

-	Layers:
	-	`sha256:4292e75d9c32bf0ba80c2339d71516e065e70a4058f12e0d895837e96fa29963`  
		Last Modified: Wed, 13 Nov 2024 01:53:01 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; ppc64le

```console
$ docker pull nats@sha256:bfc123cdde6254307ee92ec40bfec41601825fb47a75326b4360f44bab372a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe22c4f1bea64db8b0f24a64002aa2061b73145c74e4218b813d0639491ea37`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:76bf2b5924879fa33a4c81c16fab61afb5d237715cb64ef9e8847f5b8cd91151`  
		Last Modified: Thu, 17 Oct 2024 18:09:44 GMT  
		Size: 5.3 MB (5279091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22806de38895554cf572cdc72c340ce1c2a1e339ea920a8fd272f6908805d555`  
		Last Modified: Tue, 12 Nov 2024 15:01:33 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:c68e4834537eedd18677a7ba9c608218c21721b078d08969c0d9c47a48e5a2bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6620d942923f41e16c63215620c4590dade6c160c8b3464748128fc3f4fe9f1`

```dockerfile
```

-	Layers:
	-	`sha256:f936acbf9b3ac4e546df2f3f5b7c04867dfd20bc3b0efd62c5b655a66d588f46`  
		Last Modified: Tue, 12 Nov 2024 15:01:33 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; s390x

```console
$ docker pull nats@sha256:860ac3f0cce933e2518b5dfad7e4ceb5d0a65e5e4958848ea12f0e2cf6262e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b1957d328a071a836284d4b15fee34cc4d49960896e4f141a5d8ff677d654e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fffb3288c2f56b83007e69c7219ef513ffc8b9f7f218885669a4d81f7aea10c7`  
		Last Modified: Thu, 17 Oct 2024 18:09:45 GMT  
		Size: 5.6 MB (5603688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2fd1adb449a2e37ee7766e0822200ce9fef4742f0a63f4271d9db4b8e2f3f1`  
		Last Modified: Tue, 12 Nov 2024 22:35:30 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:0f6e8d82de7f4a5a2d5fc517757ceaf8a2a1411abfc8fdc89d44e7a32f7c1ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67bf5d4378b516209f4da80c21451bb69cbb934cf3b8d37e72dfbab1a5bb6c44`

```dockerfile
```

-	Layers:
	-	`sha256:236407df6864bbf886cc676be754b255160b1a1aece15f8331b5062b41bc981e`  
		Last Modified: Tue, 12 Nov 2024 22:35:30 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:af099d0ad09f68427f6716cbe03227c5409000f9021c92a4981a6099e9901dc7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161090154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e23925b656567c9ef8ee2bc478e0ada3269421cc962f905108b7ac70bfc5d2f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Thu, 14 Nov 2024 21:26:06 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 14 Nov 2024 21:26:11 GMT
RUN cmd /S /C #(nop) COPY file:6efa011ff84014d148ada9315a3292149a71c3daa1b536499f2b43a2daee2d50 in C:\nats-server.exe 
# Thu, 14 Nov 2024 21:26:12 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Nov 2024 21:26:12 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 14 Nov 2024 21:26:13 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Nov 2024 21:26:14 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077c935cc00e1acf8d3769c81d23f3134507c1149593f2af1de160f98fd769e3`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb87536f0d2cb71d86892dcf0a7036c92d682cdf7e3a8dadda31d9569a62118`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 5.9 MB (5870083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929a1f4fa9be7e6e28a451ae8e437938d70bb70ab75539f175ac46be518d2292`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d64f781d33814e56a5a3e633b6778e34fb06d03ee0cf92a7b1931ffea43af5`  
		Last Modified: Thu, 14 Nov 2024 21:26:16 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f881ff7235bc92d60a608d0336719df84a7f2a45c17ef58277f678e69e3acb1b`  
		Last Modified: Thu, 14 Nov 2024 21:26:16 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d5e5b49ab6c4788712962e67498e176b4fdb803f692b97a96580ca87f612c`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:28de350897b589b46cbe9be25abd075eaad0faeb45ab4b1c832d1fa0dcf28d6d
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

### `nats:2.10-alpine` - linux; amd64

```console
$ docker pull nats@sha256:1fd834581735b304465d440d706f668b245fa15c90864a8110d0069628504799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10017410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69bad2eb78b7ad191ae578a8cd1a90bb014cd770b959fdf75228696af9e957b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3eb8f37ad7a3d0e0d42022d3b399dbeb45f39b9a36dd95f9c74eb3ee4ff505`  
		Last Modified: Tue, 10 Dec 2024 23:27:27 GMT  
		Size: 6.4 MB (6371998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d30e571e9a33b90d53adc364b75dc4175a04f59de9d03895a30448068789fd`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64e4621359f08beab60eaf8e077f6f6ab0cec1ab6c999d1fdb4b35235662973`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:205d307881aedf2bd51cd9499b2e7cab47ada6b75a95df123216ad185b195a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9195c0eaed762824d5c53e56fe0b79a7d0d6375197aea07ffe383a513bb9a998`

```dockerfile
```

-	Layers:
	-	`sha256:069960ecffcdfc8e80d9352cfbe93b35fda077faf6c558950c05b3be76d07796`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:3569b3c6c6049c65c064d2c1638f58c6373d9779bfbafa529c82b117df449f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9387859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78fb87af3390f4d569e90248e5ef868c71ea224696608d9676420a21f08204f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d491d6ae32f791b6c6ee444da2433c3fe5f68f95a28a063e08fba789ebeb3f1`  
		Last Modified: Tue, 10 Dec 2024 23:27:13 GMT  
		Size: 6.0 MB (6019710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865e30e55f10109ec4fa649ff5598bb63785974f48e3467909963032f1b75bf3`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e27652e6cdf62ea6391042bda7e59583d83826301e119078799dc7674d5f916`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5c9032bdc8ef63d822723910e03076cf5c904847843dde7aa3597eb73c844ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4723e93aa61b1d00a73afea3fa2d282ca9b9cfbf288b20c9edb846ddc14746`

```dockerfile
```

-	Layers:
	-	`sha256:e07ee39720e7781ee4b9ccfe13bf58df6e7045efc1ed482c9f6a811ceb5c4cb0`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a0825f66cb5b9d7837459726ec6ca63a60b3888e8b67c655c7bd4c0ba05448cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9108253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9dd517c3a03af5824c23a81cedeed2598c4db1f301b3bc2e9bc40f4ab1bd618`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c84334747ecb5ce1375e80f91f5c140846eb6d7d51f9f6e6706641e1534c47`  
		Last Modified: Tue, 10 Dec 2024 23:27:11 GMT  
		Size: 6.0 MB (6007249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8010f8f3390c5e4323711c7f680070162d24e7fe3a14cf0e3d4670bd86647f9f`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573b54805f27aadae125876129ffbe488c10a85a15c36f50824d9ea4120537db`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6332c66401722e3837a6d186f7f9e1998a51350aa4b0af94507fbabb700ebb51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8a5df688f658118f4802867e4073818b174fd568574578a38138431bcbe412`

```dockerfile
```

-	Layers:
	-	`sha256:90edcaab6c14939090cda88a4bafbf0f09deddae7ca690ec3b1cda3e66db02a9`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:44905153cfe19be67e2baf248d1fe4a687aa2542e28efbff0f08f466e8749d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9912066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18b42869bfcbe5193535e39dc5571d303f0fcfd8c8fef4c6bb885ebe9b16b70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab592abba0f5f4ec119ae6d68f1206012d0485e97bb32949ec2a5bd04eb22f6`  
		Last Modified: Tue, 10 Dec 2024 23:27:05 GMT  
		Size: 5.9 MB (5917911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83961d61cdbd8298afd926b21e9e703be42edad95c17d626d5b2c8f8bdfafca`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403efcdcd91f4b94baeb36d579d722af0241889ee36afa8b92229b2c6eb937b4`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a25a621ca70ce2b0b97e30ce8ff0dbaed26cdf192d3a9f357bee0ee044c610d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850950126604011113cf97360a1b385355861ecabbe661483a1173cd8dd61172`

```dockerfile
```

-	Layers:
	-	`sha256:92f99c76a992a8785e402afdc8c8fee96331b60410b4a73baacc424b5d4ef722`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:d23003b22072b07cea7c57403d30519c9974445420181d8e174fbfa45fa533ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b0b23cf06fe3a7a78cbf9050f6de38b3cbd86fd9eadd9aa0b576d10af31480`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aaaa26dccaea10b5b83d01ed56f7a196c902179c89f7b031693a66884d17aef`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 5.7 MB (5738932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd34510b2845266284f593caae986bea90464fb438d79811c16c21afc268db9`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2beb0025099f5180f9671beb5f58c8b9fb8950f5971472ca2aded6d8c086dfcc`  
		Last Modified: Tue, 12 Nov 2024 03:03:02 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6ff0dd9b59f440e98ec6d6043cae3c81909695d9cf72e4f75ee2729e8104db86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72e08b6ff60c9977edbbe63a98b79f532617da8c1b3435d620244dd54347bea`

```dockerfile
```

-	Layers:
	-	`sha256:5f8a5a969359fee4a9f6bfec8cf77271b3a9243079c36ba7fbda1fadd5e0130c`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; s390x

```console
$ docker pull nats@sha256:d62285e97415380d73c75ff154d35fa1c6d6bec23a71995a671e665405d855b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9687191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658e5ca2d2437afce8173f52960e6280cfc673cd68edd78c9b60d8e50f94624b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f889b72b6e6f2f7a8f55853722d58f9f51fb766899e07465539676a22f0ca84`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 6.2 MB (6216702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995a4bc6424d4d94211f245dfd6f8f7975eea36b074521a866fbb75000ae79cd`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2990cf750e1e6ae965cb5ee3aa09fb5555f8709d7b9fd091ff70f124dd53a69d`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ef1002190acf6bcefe4da93459355df9b9bd492b52bf5895f710fadb82698c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bbee94701029b1f45fcbe9dbe8783e933466d45dd6eeefdb23d66cbb64483b5`

```dockerfile
```

-	Layers:
	-	`sha256:8c627f5f6e115176dd03af0a018e19fad71b8bb00277a4792730d383bd1e9868`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-alpine3.21`

```console
$ docker pull nats@sha256:87ed4c1ce118ac91e10e8b917c75085959d008a69219f32a0ddd3f31619b1adf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10-alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:1fd834581735b304465d440d706f668b245fa15c90864a8110d0069628504799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10017410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69bad2eb78b7ad191ae578a8cd1a90bb014cd770b959fdf75228696af9e957b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3eb8f37ad7a3d0e0d42022d3b399dbeb45f39b9a36dd95f9c74eb3ee4ff505`  
		Last Modified: Tue, 10 Dec 2024 23:27:27 GMT  
		Size: 6.4 MB (6371998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d30e571e9a33b90d53adc364b75dc4175a04f59de9d03895a30448068789fd`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64e4621359f08beab60eaf8e077f6f6ab0cec1ab6c999d1fdb4b35235662973`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:205d307881aedf2bd51cd9499b2e7cab47ada6b75a95df123216ad185b195a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9195c0eaed762824d5c53e56fe0b79a7d0d6375197aea07ffe383a513bb9a998`

```dockerfile
```

-	Layers:
	-	`sha256:069960ecffcdfc8e80d9352cfbe93b35fda077faf6c558950c05b3be76d07796`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:3569b3c6c6049c65c064d2c1638f58c6373d9779bfbafa529c82b117df449f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9387859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78fb87af3390f4d569e90248e5ef868c71ea224696608d9676420a21f08204f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d491d6ae32f791b6c6ee444da2433c3fe5f68f95a28a063e08fba789ebeb3f1`  
		Last Modified: Tue, 10 Dec 2024 23:27:13 GMT  
		Size: 6.0 MB (6019710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865e30e55f10109ec4fa649ff5598bb63785974f48e3467909963032f1b75bf3`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e27652e6cdf62ea6391042bda7e59583d83826301e119078799dc7674d5f916`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:5c9032bdc8ef63d822723910e03076cf5c904847843dde7aa3597eb73c844ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4723e93aa61b1d00a73afea3fa2d282ca9b9cfbf288b20c9edb846ddc14746`

```dockerfile
```

-	Layers:
	-	`sha256:e07ee39720e7781ee4b9ccfe13bf58df6e7045efc1ed482c9f6a811ceb5c4cb0`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:a0825f66cb5b9d7837459726ec6ca63a60b3888e8b67c655c7bd4c0ba05448cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9108253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9dd517c3a03af5824c23a81cedeed2598c4db1f301b3bc2e9bc40f4ab1bd618`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c84334747ecb5ce1375e80f91f5c140846eb6d7d51f9f6e6706641e1534c47`  
		Last Modified: Tue, 10 Dec 2024 23:27:11 GMT  
		Size: 6.0 MB (6007249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8010f8f3390c5e4323711c7f680070162d24e7fe3a14cf0e3d4670bd86647f9f`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573b54805f27aadae125876129ffbe488c10a85a15c36f50824d9ea4120537db`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:6332c66401722e3837a6d186f7f9e1998a51350aa4b0af94507fbabb700ebb51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8a5df688f658118f4802867e4073818b174fd568574578a38138431bcbe412`

```dockerfile
```

-	Layers:
	-	`sha256:90edcaab6c14939090cda88a4bafbf0f09deddae7ca690ec3b1cda3e66db02a9`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:44905153cfe19be67e2baf248d1fe4a687aa2542e28efbff0f08f466e8749d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9912066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18b42869bfcbe5193535e39dc5571d303f0fcfd8c8fef4c6bb885ebe9b16b70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab592abba0f5f4ec119ae6d68f1206012d0485e97bb32949ec2a5bd04eb22f6`  
		Last Modified: Tue, 10 Dec 2024 23:27:05 GMT  
		Size: 5.9 MB (5917911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83961d61cdbd8298afd926b21e9e703be42edad95c17d626d5b2c8f8bdfafca`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403efcdcd91f4b94baeb36d579d722af0241889ee36afa8b92229b2c6eb937b4`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:a25a621ca70ce2b0b97e30ce8ff0dbaed26cdf192d3a9f357bee0ee044c610d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850950126604011113cf97360a1b385355861ecabbe661483a1173cd8dd61172`

```dockerfile
```

-	Layers:
	-	`sha256:92f99c76a992a8785e402afdc8c8fee96331b60410b4a73baacc424b5d4ef722`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:d62285e97415380d73c75ff154d35fa1c6d6bec23a71995a671e665405d855b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9687191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658e5ca2d2437afce8173f52960e6280cfc673cd68edd78c9b60d8e50f94624b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f889b72b6e6f2f7a8f55853722d58f9f51fb766899e07465539676a22f0ca84`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 6.2 MB (6216702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995a4bc6424d4d94211f245dfd6f8f7975eea36b074521a866fbb75000ae79cd`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2990cf750e1e6ae965cb5ee3aa09fb5555f8709d7b9fd091ff70f124dd53a69d`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:ef1002190acf6bcefe4da93459355df9b9bd492b52bf5895f710fadb82698c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bbee94701029b1f45fcbe9dbe8783e933466d45dd6eeefdb23d66cbb64483b5`

```dockerfile
```

-	Layers:
	-	`sha256:8c627f5f6e115176dd03af0a018e19fad71b8bb00277a4792730d383bd1e9868`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:23638865a8c200681a3a58ee86cd9c5776bbc7499f5525ce9c9baae4d4970d2a
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

### `nats:2.10-linux` - linux; amd64

```console
$ docker pull nats@sha256:26b0ee1a95285aedae137aefb953701d9da1dfffcf7818eb3aeb536c4373892f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9321c727224d6919153399a2554913ee3ea75615c40faf0b0b61719fd4cba18f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc7b6eeb42db27589fb02b7af7648621b4230b391664f1cabca731c0cb74c6c0`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.7 MB (5748809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648a1fe081b19052a39d36fde23ff89c48a0b60bddc52cdf58474ed9b7e16ab4`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:92b63acf1eb46cb3ce90a6406fcf9cf3214ba330e4dacef512280529a04870ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd7260fa709b7a3bb731d03f1fc89313f81c37eaacc9a95aef394dde1aa26ae`

```dockerfile
```

-	Layers:
	-	`sha256:eb1f99c4d9cf8c2d861e264c9ba0cdb9161bb70c2764c955ab1f90310af1f472`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:ed0d3d3f325c395d64fe3cce644fcb8a85dd7f693321155adc742f9a4558a524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5414498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb43c0fb21e266dce12015b728c78e144c79b548aa91729dffae13470e0d9297`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:359939d6b9b0e79cd20ca9621811c48e03c3d4a5b7af0a099486d520bf5d7b5f`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.4 MB (5413989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f789fb3e9d2d0ff4362d663dece6c6656816327c3c477f706bb39361ec1cd75`  
		Last Modified: Tue, 12 Nov 2024 15:37:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:6ed1504d0cb0d9a7e50ccb85fa202b5d8901dc4bc331ec9212598e39c7cb9708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35958b08d07b59577364ce756c66f53782d4b469b1eb5fa49f8e1d5b54cdca4`

```dockerfile
```

-	Layers:
	-	`sha256:4666424ba74b452fb83d3ee0779517652e5b5c382cd17ac41b3a6eed5fa553c9`  
		Last Modified: Tue, 12 Nov 2024 15:37:52 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:6e124d1272a57524b4ca6d20f067a1bcaaf0698436552c1e023098e8d86f3ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5402382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48a99f0a97426e5e74f3a25a607b2c16d9a4521a32a2ba12fa6fdd0202e4bf5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d05d846e8109608ff47e05c22bb31057b6b6430dcabb8110890869d111bd1b9e`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.4 MB (5401872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2f51350cd72f7f51dbac3739d56b990a14dbbf86618c4893c441ddc4b1bb8c`  
		Last Modified: Wed, 13 Nov 2024 06:50:55 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:8961a748bcb9e725a669f8fa2f9feb42d333982353b703fc2ab7d1dcc75672df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f520b399deef237b5cb2d8124b151ec2c5226e54324dd079da79164fb174dba`

```dockerfile
```

-	Layers:
	-	`sha256:1eee6a8956b4ad976df210a755d0ef0e99d56f92ba24d749b7da0611fad96580`  
		Last Modified: Wed, 13 Nov 2024 06:50:55 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a472fd5123d4894808a5300ae620b1fc75173683a27bef46da8f72cffc933c98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5311420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b2641c24dab528ab7f50965ba60bf552fd0741d08bce6d7eb119bdb14c2eb9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:38a1a08cf356fa2c344f9efdd2f487176ba47d86dbe408ea24116528e7638b79`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.3 MB (5310912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f500aab43d6d7fb9af41817fd3e6d15af8d2cea39f195b594bb2aaf7ea3f8a3e`  
		Last Modified: Wed, 13 Nov 2024 01:53:01 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:28b2143fc08c4b9fa3086b9adbeb584e61f0fd522723dab3544ba1cf8d69f896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b61c129357d5acdec05b9878360c584d3e152bff6203d60fb73bba1d793c8f`

```dockerfile
```

-	Layers:
	-	`sha256:4292e75d9c32bf0ba80c2339d71516e065e70a4058f12e0d895837e96fa29963`  
		Last Modified: Wed, 13 Nov 2024 01:53:01 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:bfc123cdde6254307ee92ec40bfec41601825fb47a75326b4360f44bab372a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe22c4f1bea64db8b0f24a64002aa2061b73145c74e4218b813d0639491ea37`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:76bf2b5924879fa33a4c81c16fab61afb5d237715cb64ef9e8847f5b8cd91151`  
		Last Modified: Thu, 17 Oct 2024 18:09:44 GMT  
		Size: 5.3 MB (5279091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22806de38895554cf572cdc72c340ce1c2a1e339ea920a8fd272f6908805d555`  
		Last Modified: Tue, 12 Nov 2024 15:01:33 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:c68e4834537eedd18677a7ba9c608218c21721b078d08969c0d9c47a48e5a2bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6620d942923f41e16c63215620c4590dade6c160c8b3464748128fc3f4fe9f1`

```dockerfile
```

-	Layers:
	-	`sha256:f936acbf9b3ac4e546df2f3f5b7c04867dfd20bc3b0efd62c5b655a66d588f46`  
		Last Modified: Tue, 12 Nov 2024 15:01:33 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; s390x

```console
$ docker pull nats@sha256:860ac3f0cce933e2518b5dfad7e4ceb5d0a65e5e4958848ea12f0e2cf6262e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b1957d328a071a836284d4b15fee34cc4d49960896e4f141a5d8ff677d654e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fffb3288c2f56b83007e69c7219ef513ffc8b9f7f218885669a4d81f7aea10c7`  
		Last Modified: Thu, 17 Oct 2024 18:09:45 GMT  
		Size: 5.6 MB (5603688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2fd1adb449a2e37ee7766e0822200ce9fef4742f0a63f4271d9db4b8e2f3f1`  
		Last Modified: Tue, 12 Nov 2024 22:35:30 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:0f6e8d82de7f4a5a2d5fc517757ceaf8a2a1411abfc8fdc89d44e7a32f7c1ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67bf5d4378b516209f4da80c21451bb69cbb934cf3b8d37e72dfbab1a5bb6c44`

```dockerfile
```

-	Layers:
	-	`sha256:236407df6864bbf886cc676be754b255160b1a1aece15f8331b5062b41bc981e`  
		Last Modified: Tue, 12 Nov 2024 22:35:30 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-nanoserver`

```console
$ docker pull nats@sha256:070f9e269bf92f0bedac63b5a0f269f7520ad54e071f7953b5c35621160ad025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `nats:2.10-nanoserver` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:af099d0ad09f68427f6716cbe03227c5409000f9021c92a4981a6099e9901dc7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161090154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e23925b656567c9ef8ee2bc478e0ada3269421cc962f905108b7ac70bfc5d2f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Thu, 14 Nov 2024 21:26:06 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 14 Nov 2024 21:26:11 GMT
RUN cmd /S /C #(nop) COPY file:6efa011ff84014d148ada9315a3292149a71c3daa1b536499f2b43a2daee2d50 in C:\nats-server.exe 
# Thu, 14 Nov 2024 21:26:12 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Nov 2024 21:26:12 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 14 Nov 2024 21:26:13 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Nov 2024 21:26:14 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077c935cc00e1acf8d3769c81d23f3134507c1149593f2af1de160f98fd769e3`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb87536f0d2cb71d86892dcf0a7036c92d682cdf7e3a8dadda31d9569a62118`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 5.9 MB (5870083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929a1f4fa9be7e6e28a451ae8e437938d70bb70ab75539f175ac46be518d2292`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d64f781d33814e56a5a3e633b6778e34fb06d03ee0cf92a7b1931ffea43af5`  
		Last Modified: Thu, 14 Nov 2024 21:26:16 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f881ff7235bc92d60a608d0336719df84a7f2a45c17ef58277f678e69e3acb1b`  
		Last Modified: Thu, 14 Nov 2024 21:26:16 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d5e5b49ab6c4788712962e67498e176b4fdb803f692b97a96580ca87f612c`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-1809`

```console
$ docker pull nats@sha256:070f9e269bf92f0bedac63b5a0f269f7520ad54e071f7953b5c35621160ad025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `nats:2.10-nanoserver-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:af099d0ad09f68427f6716cbe03227c5409000f9021c92a4981a6099e9901dc7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161090154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e23925b656567c9ef8ee2bc478e0ada3269421cc962f905108b7ac70bfc5d2f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Thu, 14 Nov 2024 21:26:06 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 14 Nov 2024 21:26:11 GMT
RUN cmd /S /C #(nop) COPY file:6efa011ff84014d148ada9315a3292149a71c3daa1b536499f2b43a2daee2d50 in C:\nats-server.exe 
# Thu, 14 Nov 2024 21:26:12 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Nov 2024 21:26:12 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 14 Nov 2024 21:26:13 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Nov 2024 21:26:14 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077c935cc00e1acf8d3769c81d23f3134507c1149593f2af1de160f98fd769e3`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb87536f0d2cb71d86892dcf0a7036c92d682cdf7e3a8dadda31d9569a62118`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 5.9 MB (5870083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929a1f4fa9be7e6e28a451ae8e437938d70bb70ab75539f175ac46be518d2292`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d64f781d33814e56a5a3e633b6778e34fb06d03ee0cf92a7b1931ffea43af5`  
		Last Modified: Thu, 14 Nov 2024 21:26:16 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f881ff7235bc92d60a608d0336719df84a7f2a45c17ef58277f678e69e3acb1b`  
		Last Modified: Thu, 14 Nov 2024 21:26:16 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d5e5b49ab6c4788712962e67498e176b4fdb803f692b97a96580ca87f612c`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-scratch`

```console
$ docker pull nats@sha256:23638865a8c200681a3a58ee86cd9c5776bbc7499f5525ce9c9baae4d4970d2a
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

### `nats:2.10-scratch` - linux; amd64

```console
$ docker pull nats@sha256:26b0ee1a95285aedae137aefb953701d9da1dfffcf7818eb3aeb536c4373892f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9321c727224d6919153399a2554913ee3ea75615c40faf0b0b61719fd4cba18f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc7b6eeb42db27589fb02b7af7648621b4230b391664f1cabca731c0cb74c6c0`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.7 MB (5748809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648a1fe081b19052a39d36fde23ff89c48a0b60bddc52cdf58474ed9b7e16ab4`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:92b63acf1eb46cb3ce90a6406fcf9cf3214ba330e4dacef512280529a04870ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd7260fa709b7a3bb731d03f1fc89313f81c37eaacc9a95aef394dde1aa26ae`

```dockerfile
```

-	Layers:
	-	`sha256:eb1f99c4d9cf8c2d861e264c9ba0cdb9161bb70c2764c955ab1f90310af1f472`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:ed0d3d3f325c395d64fe3cce644fcb8a85dd7f693321155adc742f9a4558a524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5414498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb43c0fb21e266dce12015b728c78e144c79b548aa91729dffae13470e0d9297`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:359939d6b9b0e79cd20ca9621811c48e03c3d4a5b7af0a099486d520bf5d7b5f`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.4 MB (5413989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f789fb3e9d2d0ff4362d663dece6c6656816327c3c477f706bb39361ec1cd75`  
		Last Modified: Tue, 12 Nov 2024 15:37:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:6ed1504d0cb0d9a7e50ccb85fa202b5d8901dc4bc331ec9212598e39c7cb9708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35958b08d07b59577364ce756c66f53782d4b469b1eb5fa49f8e1d5b54cdca4`

```dockerfile
```

-	Layers:
	-	`sha256:4666424ba74b452fb83d3ee0779517652e5b5c382cd17ac41b3a6eed5fa553c9`  
		Last Modified: Tue, 12 Nov 2024 15:37:52 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:6e124d1272a57524b4ca6d20f067a1bcaaf0698436552c1e023098e8d86f3ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5402382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48a99f0a97426e5e74f3a25a607b2c16d9a4521a32a2ba12fa6fdd0202e4bf5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d05d846e8109608ff47e05c22bb31057b6b6430dcabb8110890869d111bd1b9e`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.4 MB (5401872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2f51350cd72f7f51dbac3739d56b990a14dbbf86618c4893c441ddc4b1bb8c`  
		Last Modified: Wed, 13 Nov 2024 06:50:55 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:8961a748bcb9e725a669f8fa2f9feb42d333982353b703fc2ab7d1dcc75672df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f520b399deef237b5cb2d8124b151ec2c5226e54324dd079da79164fb174dba`

```dockerfile
```

-	Layers:
	-	`sha256:1eee6a8956b4ad976df210a755d0ef0e99d56f92ba24d749b7da0611fad96580`  
		Last Modified: Wed, 13 Nov 2024 06:50:55 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a472fd5123d4894808a5300ae620b1fc75173683a27bef46da8f72cffc933c98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5311420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b2641c24dab528ab7f50965ba60bf552fd0741d08bce6d7eb119bdb14c2eb9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:38a1a08cf356fa2c344f9efdd2f487176ba47d86dbe408ea24116528e7638b79`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.3 MB (5310912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f500aab43d6d7fb9af41817fd3e6d15af8d2cea39f195b594bb2aaf7ea3f8a3e`  
		Last Modified: Wed, 13 Nov 2024 01:53:01 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:28b2143fc08c4b9fa3086b9adbeb584e61f0fd522723dab3544ba1cf8d69f896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b61c129357d5acdec05b9878360c584d3e152bff6203d60fb73bba1d793c8f`

```dockerfile
```

-	Layers:
	-	`sha256:4292e75d9c32bf0ba80c2339d71516e065e70a4058f12e0d895837e96fa29963`  
		Last Modified: Wed, 13 Nov 2024 01:53:01 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:bfc123cdde6254307ee92ec40bfec41601825fb47a75326b4360f44bab372a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe22c4f1bea64db8b0f24a64002aa2061b73145c74e4218b813d0639491ea37`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:76bf2b5924879fa33a4c81c16fab61afb5d237715cb64ef9e8847f5b8cd91151`  
		Last Modified: Thu, 17 Oct 2024 18:09:44 GMT  
		Size: 5.3 MB (5279091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22806de38895554cf572cdc72c340ce1c2a1e339ea920a8fd272f6908805d555`  
		Last Modified: Tue, 12 Nov 2024 15:01:33 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:c68e4834537eedd18677a7ba9c608218c21721b078d08969c0d9c47a48e5a2bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6620d942923f41e16c63215620c4590dade6c160c8b3464748128fc3f4fe9f1`

```dockerfile
```

-	Layers:
	-	`sha256:f936acbf9b3ac4e546df2f3f5b7c04867dfd20bc3b0efd62c5b655a66d588f46`  
		Last Modified: Tue, 12 Nov 2024 15:01:33 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; s390x

```console
$ docker pull nats@sha256:860ac3f0cce933e2518b5dfad7e4ceb5d0a65e5e4958848ea12f0e2cf6262e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b1957d328a071a836284d4b15fee34cc4d49960896e4f141a5d8ff677d654e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fffb3288c2f56b83007e69c7219ef513ffc8b9f7f218885669a4d81f7aea10c7`  
		Last Modified: Thu, 17 Oct 2024 18:09:45 GMT  
		Size: 5.6 MB (5603688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2fd1adb449a2e37ee7766e0822200ce9fef4742f0a63f4271d9db4b8e2f3f1`  
		Last Modified: Tue, 12 Nov 2024 22:35:30 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:0f6e8d82de7f4a5a2d5fc517757ceaf8a2a1411abfc8fdc89d44e7a32f7c1ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67bf5d4378b516209f4da80c21451bb69cbb934cf3b8d37e72dfbab1a5bb6c44`

```dockerfile
```

-	Layers:
	-	`sha256:236407df6864bbf886cc676be754b255160b1a1aece15f8331b5062b41bc981e`  
		Last Modified: Tue, 12 Nov 2024 22:35:30 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-windowsservercore`

```console
$ docker pull nats@sha256:43fbcf8dfa35b4760178e0b4e16c2474d68f1ab3128b980817133057582d7e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:d8404f289d887ce07c6ec8c2ed3f2512727f6d6d33791e6f0d607f03a7bb99d0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2017532110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91991216a6a1544d8f469907d8e4e7e7aeb83722aa7f22591fb24566360cc0ab`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Tue, 10 Dec 2024 23:27:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Dec 2024 23:27:31 GMT
ENV NATS_DOCKERIZED=1
# Tue, 10 Dec 2024 23:27:32 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 23:27:32 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.23/nats-server-v2.10.23-windows-amd64.zip
# Tue, 10 Dec 2024 23:27:33 GMT
ENV NATS_SERVER_SHASUM=4ec39c0df08823a062dcdaac23ccf7ee56e76ccc27b69134f3e9b1549bc0f305
# Tue, 10 Dec 2024 23:28:50 GMT
RUN Set-PSDebug -Trace 2
# Tue, 10 Dec 2024 23:29:14 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 10 Dec 2024 23:29:14 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 10 Dec 2024 23:29:15 GMT
EXPOSE 4222 6222 8222
# Tue, 10 Dec 2024 23:29:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Dec 2024 23:29:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05963517ca3d5c411c11e9cf4ac529f3affa194a7f0914374d3b98008e19fcd`  
		Last Modified: Tue, 10 Dec 2024 23:29:20 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d8577eb6f25bb0f27f3d64f76584102e62ec7d909b34960f3f37f832653a0e`  
		Last Modified: Tue, 10 Dec 2024 23:29:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d70b39f16077baba91f50f30b3e69fbb08e38919da455c6ab5aad8d102b0a4`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231308f503d04392a55f1811db0102c1873660ab3780d766220170f78845628d`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8454af0dc55c7414c29902b1ae692d77206dbf2d5e0329ea7f4d00b32e43981f`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae10fbf74e9db38c4b611d58d3aabebe4336ef55f067d024a5753990d8ee0c65`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 485.0 KB (485022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b00a4239ecfe83a559cd5f40ff7a390b535f2c4a718c1dfcb11fb36e643bc6`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 6.4 MB (6381052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293d2ecab9ac866fa0d9cd648139d9576b12e77960c11dd976d1e874a69074e3`  
		Last Modified: Tue, 10 Dec 2024 23:29:18 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcaf4545aa895aefcb8f088f2fada2e81ed4f5ea5070c634da65a3226c5f454d`  
		Last Modified: Tue, 10 Dec 2024 23:29:18 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be99fe33f983eb453fe8c100eb4bc03e6d17392e701deae38cf0dcb416b86635`  
		Last Modified: Tue, 10 Dec 2024 23:29:18 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ace41bfa487712fd128caaa0b1ddb268f5cc6f198c990a822fa0b9a55c0cee7`  
		Last Modified: Tue, 10 Dec 2024 23:29:18 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-1809`

```console
$ docker pull nats@sha256:43fbcf8dfa35b4760178e0b4e16c2474d68f1ab3128b980817133057582d7e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `nats:2.10-windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:d8404f289d887ce07c6ec8c2ed3f2512727f6d6d33791e6f0d607f03a7bb99d0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2017532110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91991216a6a1544d8f469907d8e4e7e7aeb83722aa7f22591fb24566360cc0ab`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Tue, 10 Dec 2024 23:27:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Dec 2024 23:27:31 GMT
ENV NATS_DOCKERIZED=1
# Tue, 10 Dec 2024 23:27:32 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 23:27:32 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.23/nats-server-v2.10.23-windows-amd64.zip
# Tue, 10 Dec 2024 23:27:33 GMT
ENV NATS_SERVER_SHASUM=4ec39c0df08823a062dcdaac23ccf7ee56e76ccc27b69134f3e9b1549bc0f305
# Tue, 10 Dec 2024 23:28:50 GMT
RUN Set-PSDebug -Trace 2
# Tue, 10 Dec 2024 23:29:14 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 10 Dec 2024 23:29:14 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 10 Dec 2024 23:29:15 GMT
EXPOSE 4222 6222 8222
# Tue, 10 Dec 2024 23:29:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Dec 2024 23:29:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05963517ca3d5c411c11e9cf4ac529f3affa194a7f0914374d3b98008e19fcd`  
		Last Modified: Tue, 10 Dec 2024 23:29:20 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d8577eb6f25bb0f27f3d64f76584102e62ec7d909b34960f3f37f832653a0e`  
		Last Modified: Tue, 10 Dec 2024 23:29:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d70b39f16077baba91f50f30b3e69fbb08e38919da455c6ab5aad8d102b0a4`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231308f503d04392a55f1811db0102c1873660ab3780d766220170f78845628d`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8454af0dc55c7414c29902b1ae692d77206dbf2d5e0329ea7f4d00b32e43981f`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae10fbf74e9db38c4b611d58d3aabebe4336ef55f067d024a5753990d8ee0c65`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 485.0 KB (485022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b00a4239ecfe83a559cd5f40ff7a390b535f2c4a718c1dfcb11fb36e643bc6`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 6.4 MB (6381052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293d2ecab9ac866fa0d9cd648139d9576b12e77960c11dd976d1e874a69074e3`  
		Last Modified: Tue, 10 Dec 2024 23:29:18 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcaf4545aa895aefcb8f088f2fada2e81ed4f5ea5070c634da65a3226c5f454d`  
		Last Modified: Tue, 10 Dec 2024 23:29:18 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be99fe33f983eb453fe8c100eb4bc03e6d17392e701deae38cf0dcb416b86635`  
		Last Modified: Tue, 10 Dec 2024 23:29:18 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ace41bfa487712fd128caaa0b1ddb268f5cc6f198c990a822fa0b9a55c0cee7`  
		Last Modified: Tue, 10 Dec 2024 23:29:18 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.23`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.10.23-alpine`

```console
$ docker pull nats@sha256:87ed4c1ce118ac91e10e8b917c75085959d008a69219f32a0ddd3f31619b1adf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10.23-alpine` - linux; amd64

```console
$ docker pull nats@sha256:1fd834581735b304465d440d706f668b245fa15c90864a8110d0069628504799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10017410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69bad2eb78b7ad191ae578a8cd1a90bb014cd770b959fdf75228696af9e957b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3eb8f37ad7a3d0e0d42022d3b399dbeb45f39b9a36dd95f9c74eb3ee4ff505`  
		Last Modified: Tue, 10 Dec 2024 23:27:27 GMT  
		Size: 6.4 MB (6371998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d30e571e9a33b90d53adc364b75dc4175a04f59de9d03895a30448068789fd`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64e4621359f08beab60eaf8e077f6f6ab0cec1ab6c999d1fdb4b35235662973`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:205d307881aedf2bd51cd9499b2e7cab47ada6b75a95df123216ad185b195a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9195c0eaed762824d5c53e56fe0b79a7d0d6375197aea07ffe383a513bb9a998`

```dockerfile
```

-	Layers:
	-	`sha256:069960ecffcdfc8e80d9352cfbe93b35fda077faf6c558950c05b3be76d07796`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.23-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:3569b3c6c6049c65c064d2c1638f58c6373d9779bfbafa529c82b117df449f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9387859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78fb87af3390f4d569e90248e5ef868c71ea224696608d9676420a21f08204f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d491d6ae32f791b6c6ee444da2433c3fe5f68f95a28a063e08fba789ebeb3f1`  
		Last Modified: Tue, 10 Dec 2024 23:27:13 GMT  
		Size: 6.0 MB (6019710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865e30e55f10109ec4fa649ff5598bb63785974f48e3467909963032f1b75bf3`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e27652e6cdf62ea6391042bda7e59583d83826301e119078799dc7674d5f916`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5c9032bdc8ef63d822723910e03076cf5c904847843dde7aa3597eb73c844ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4723e93aa61b1d00a73afea3fa2d282ca9b9cfbf288b20c9edb846ddc14746`

```dockerfile
```

-	Layers:
	-	`sha256:e07ee39720e7781ee4b9ccfe13bf58df6e7045efc1ed482c9f6a811ceb5c4cb0`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.23-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a0825f66cb5b9d7837459726ec6ca63a60b3888e8b67c655c7bd4c0ba05448cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9108253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9dd517c3a03af5824c23a81cedeed2598c4db1f301b3bc2e9bc40f4ab1bd618`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c84334747ecb5ce1375e80f91f5c140846eb6d7d51f9f6e6706641e1534c47`  
		Last Modified: Tue, 10 Dec 2024 23:27:11 GMT  
		Size: 6.0 MB (6007249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8010f8f3390c5e4323711c7f680070162d24e7fe3a14cf0e3d4670bd86647f9f`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573b54805f27aadae125876129ffbe488c10a85a15c36f50824d9ea4120537db`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6332c66401722e3837a6d186f7f9e1998a51350aa4b0af94507fbabb700ebb51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8a5df688f658118f4802867e4073818b174fd568574578a38138431bcbe412`

```dockerfile
```

-	Layers:
	-	`sha256:90edcaab6c14939090cda88a4bafbf0f09deddae7ca690ec3b1cda3e66db02a9`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.23-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:44905153cfe19be67e2baf248d1fe4a687aa2542e28efbff0f08f466e8749d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9912066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18b42869bfcbe5193535e39dc5571d303f0fcfd8c8fef4c6bb885ebe9b16b70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab592abba0f5f4ec119ae6d68f1206012d0485e97bb32949ec2a5bd04eb22f6`  
		Last Modified: Tue, 10 Dec 2024 23:27:05 GMT  
		Size: 5.9 MB (5917911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83961d61cdbd8298afd926b21e9e703be42edad95c17d626d5b2c8f8bdfafca`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403efcdcd91f4b94baeb36d579d722af0241889ee36afa8b92229b2c6eb937b4`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a25a621ca70ce2b0b97e30ce8ff0dbaed26cdf192d3a9f357bee0ee044c610d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850950126604011113cf97360a1b385355861ecabbe661483a1173cd8dd61172`

```dockerfile
```

-	Layers:
	-	`sha256:92f99c76a992a8785e402afdc8c8fee96331b60410b4a73baacc424b5d4ef722`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.23-alpine` - linux; s390x

```console
$ docker pull nats@sha256:d62285e97415380d73c75ff154d35fa1c6d6bec23a71995a671e665405d855b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9687191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658e5ca2d2437afce8173f52960e6280cfc673cd68edd78c9b60d8e50f94624b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f889b72b6e6f2f7a8f55853722d58f9f51fb766899e07465539676a22f0ca84`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 6.2 MB (6216702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995a4bc6424d4d94211f245dfd6f8f7975eea36b074521a866fbb75000ae79cd`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2990cf750e1e6ae965cb5ee3aa09fb5555f8709d7b9fd091ff70f124dd53a69d`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ef1002190acf6bcefe4da93459355df9b9bd492b52bf5895f710fadb82698c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bbee94701029b1f45fcbe9dbe8783e933466d45dd6eeefdb23d66cbb64483b5`

```dockerfile
```

-	Layers:
	-	`sha256:8c627f5f6e115176dd03af0a018e19fad71b8bb00277a4792730d383bd1e9868`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.23-alpine3.21`

```console
$ docker pull nats@sha256:87ed4c1ce118ac91e10e8b917c75085959d008a69219f32a0ddd3f31619b1adf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10.23-alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:1fd834581735b304465d440d706f668b245fa15c90864a8110d0069628504799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10017410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69bad2eb78b7ad191ae578a8cd1a90bb014cd770b959fdf75228696af9e957b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3eb8f37ad7a3d0e0d42022d3b399dbeb45f39b9a36dd95f9c74eb3ee4ff505`  
		Last Modified: Tue, 10 Dec 2024 23:27:27 GMT  
		Size: 6.4 MB (6371998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d30e571e9a33b90d53adc364b75dc4175a04f59de9d03895a30448068789fd`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64e4621359f08beab60eaf8e077f6f6ab0cec1ab6c999d1fdb4b35235662973`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:205d307881aedf2bd51cd9499b2e7cab47ada6b75a95df123216ad185b195a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9195c0eaed762824d5c53e56fe0b79a7d0d6375197aea07ffe383a513bb9a998`

```dockerfile
```

-	Layers:
	-	`sha256:069960ecffcdfc8e80d9352cfbe93b35fda077faf6c558950c05b3be76d07796`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.23-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:3569b3c6c6049c65c064d2c1638f58c6373d9779bfbafa529c82b117df449f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9387859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78fb87af3390f4d569e90248e5ef868c71ea224696608d9676420a21f08204f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d491d6ae32f791b6c6ee444da2433c3fe5f68f95a28a063e08fba789ebeb3f1`  
		Last Modified: Tue, 10 Dec 2024 23:27:13 GMT  
		Size: 6.0 MB (6019710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865e30e55f10109ec4fa649ff5598bb63785974f48e3467909963032f1b75bf3`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e27652e6cdf62ea6391042bda7e59583d83826301e119078799dc7674d5f916`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:5c9032bdc8ef63d822723910e03076cf5c904847843dde7aa3597eb73c844ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4723e93aa61b1d00a73afea3fa2d282ca9b9cfbf288b20c9edb846ddc14746`

```dockerfile
```

-	Layers:
	-	`sha256:e07ee39720e7781ee4b9ccfe13bf58df6e7045efc1ed482c9f6a811ceb5c4cb0`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.23-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:a0825f66cb5b9d7837459726ec6ca63a60b3888e8b67c655c7bd4c0ba05448cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9108253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9dd517c3a03af5824c23a81cedeed2598c4db1f301b3bc2e9bc40f4ab1bd618`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c84334747ecb5ce1375e80f91f5c140846eb6d7d51f9f6e6706641e1534c47`  
		Last Modified: Tue, 10 Dec 2024 23:27:11 GMT  
		Size: 6.0 MB (6007249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8010f8f3390c5e4323711c7f680070162d24e7fe3a14cf0e3d4670bd86647f9f`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573b54805f27aadae125876129ffbe488c10a85a15c36f50824d9ea4120537db`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:6332c66401722e3837a6d186f7f9e1998a51350aa4b0af94507fbabb700ebb51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8a5df688f658118f4802867e4073818b174fd568574578a38138431bcbe412`

```dockerfile
```

-	Layers:
	-	`sha256:90edcaab6c14939090cda88a4bafbf0f09deddae7ca690ec3b1cda3e66db02a9`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.23-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:44905153cfe19be67e2baf248d1fe4a687aa2542e28efbff0f08f466e8749d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9912066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18b42869bfcbe5193535e39dc5571d303f0fcfd8c8fef4c6bb885ebe9b16b70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab592abba0f5f4ec119ae6d68f1206012d0485e97bb32949ec2a5bd04eb22f6`  
		Last Modified: Tue, 10 Dec 2024 23:27:05 GMT  
		Size: 5.9 MB (5917911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83961d61cdbd8298afd926b21e9e703be42edad95c17d626d5b2c8f8bdfafca`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403efcdcd91f4b94baeb36d579d722af0241889ee36afa8b92229b2c6eb937b4`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:a25a621ca70ce2b0b97e30ce8ff0dbaed26cdf192d3a9f357bee0ee044c610d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850950126604011113cf97360a1b385355861ecabbe661483a1173cd8dd61172`

```dockerfile
```

-	Layers:
	-	`sha256:92f99c76a992a8785e402afdc8c8fee96331b60410b4a73baacc424b5d4ef722`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.23-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:d62285e97415380d73c75ff154d35fa1c6d6bec23a71995a671e665405d855b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9687191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658e5ca2d2437afce8173f52960e6280cfc673cd68edd78c9b60d8e50f94624b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f889b72b6e6f2f7a8f55853722d58f9f51fb766899e07465539676a22f0ca84`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 6.2 MB (6216702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995a4bc6424d4d94211f245dfd6f8f7975eea36b074521a866fbb75000ae79cd`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2990cf750e1e6ae965cb5ee3aa09fb5555f8709d7b9fd091ff70f124dd53a69d`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:ef1002190acf6bcefe4da93459355df9b9bd492b52bf5895f710fadb82698c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bbee94701029b1f45fcbe9dbe8783e933466d45dd6eeefdb23d66cbb64483b5`

```dockerfile
```

-	Layers:
	-	`sha256:8c627f5f6e115176dd03af0a018e19fad71b8bb00277a4792730d383bd1e9868`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.23-linux`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.10.23-nanoserver`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.10.23-nanoserver-1809`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.10.23-scratch`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.10.23-windowsservercore`

```console
$ docker pull nats@sha256:43fbcf8dfa35b4760178e0b4e16c2474d68f1ab3128b980817133057582d7e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `nats:2.10.23-windowsservercore` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:d8404f289d887ce07c6ec8c2ed3f2512727f6d6d33791e6f0d607f03a7bb99d0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2017532110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91991216a6a1544d8f469907d8e4e7e7aeb83722aa7f22591fb24566360cc0ab`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Tue, 10 Dec 2024 23:27:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Dec 2024 23:27:31 GMT
ENV NATS_DOCKERIZED=1
# Tue, 10 Dec 2024 23:27:32 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 23:27:32 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.23/nats-server-v2.10.23-windows-amd64.zip
# Tue, 10 Dec 2024 23:27:33 GMT
ENV NATS_SERVER_SHASUM=4ec39c0df08823a062dcdaac23ccf7ee56e76ccc27b69134f3e9b1549bc0f305
# Tue, 10 Dec 2024 23:28:50 GMT
RUN Set-PSDebug -Trace 2
# Tue, 10 Dec 2024 23:29:14 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 10 Dec 2024 23:29:14 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 10 Dec 2024 23:29:15 GMT
EXPOSE 4222 6222 8222
# Tue, 10 Dec 2024 23:29:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Dec 2024 23:29:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05963517ca3d5c411c11e9cf4ac529f3affa194a7f0914374d3b98008e19fcd`  
		Last Modified: Tue, 10 Dec 2024 23:29:20 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d8577eb6f25bb0f27f3d64f76584102e62ec7d909b34960f3f37f832653a0e`  
		Last Modified: Tue, 10 Dec 2024 23:29:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d70b39f16077baba91f50f30b3e69fbb08e38919da455c6ab5aad8d102b0a4`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231308f503d04392a55f1811db0102c1873660ab3780d766220170f78845628d`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8454af0dc55c7414c29902b1ae692d77206dbf2d5e0329ea7f4d00b32e43981f`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae10fbf74e9db38c4b611d58d3aabebe4336ef55f067d024a5753990d8ee0c65`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 485.0 KB (485022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b00a4239ecfe83a559cd5f40ff7a390b535f2c4a718c1dfcb11fb36e643bc6`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 6.4 MB (6381052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293d2ecab9ac866fa0d9cd648139d9576b12e77960c11dd976d1e874a69074e3`  
		Last Modified: Tue, 10 Dec 2024 23:29:18 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcaf4545aa895aefcb8f088f2fada2e81ed4f5ea5070c634da65a3226c5f454d`  
		Last Modified: Tue, 10 Dec 2024 23:29:18 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be99fe33f983eb453fe8c100eb4bc03e6d17392e701deae38cf0dcb416b86635`  
		Last Modified: Tue, 10 Dec 2024 23:29:18 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ace41bfa487712fd128caaa0b1ddb268f5cc6f198c990a822fa0b9a55c0cee7`  
		Last Modified: Tue, 10 Dec 2024 23:29:18 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.23-windowsservercore-1809`

```console
$ docker pull nats@sha256:43fbcf8dfa35b4760178e0b4e16c2474d68f1ab3128b980817133057582d7e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `nats:2.10.23-windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:d8404f289d887ce07c6ec8c2ed3f2512727f6d6d33791e6f0d607f03a7bb99d0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2017532110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91991216a6a1544d8f469907d8e4e7e7aeb83722aa7f22591fb24566360cc0ab`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Tue, 10 Dec 2024 23:27:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Dec 2024 23:27:31 GMT
ENV NATS_DOCKERIZED=1
# Tue, 10 Dec 2024 23:27:32 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 23:27:32 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.23/nats-server-v2.10.23-windows-amd64.zip
# Tue, 10 Dec 2024 23:27:33 GMT
ENV NATS_SERVER_SHASUM=4ec39c0df08823a062dcdaac23ccf7ee56e76ccc27b69134f3e9b1549bc0f305
# Tue, 10 Dec 2024 23:28:50 GMT
RUN Set-PSDebug -Trace 2
# Tue, 10 Dec 2024 23:29:14 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 10 Dec 2024 23:29:14 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 10 Dec 2024 23:29:15 GMT
EXPOSE 4222 6222 8222
# Tue, 10 Dec 2024 23:29:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Dec 2024 23:29:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05963517ca3d5c411c11e9cf4ac529f3affa194a7f0914374d3b98008e19fcd`  
		Last Modified: Tue, 10 Dec 2024 23:29:20 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d8577eb6f25bb0f27f3d64f76584102e62ec7d909b34960f3f37f832653a0e`  
		Last Modified: Tue, 10 Dec 2024 23:29:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d70b39f16077baba91f50f30b3e69fbb08e38919da455c6ab5aad8d102b0a4`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231308f503d04392a55f1811db0102c1873660ab3780d766220170f78845628d`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8454af0dc55c7414c29902b1ae692d77206dbf2d5e0329ea7f4d00b32e43981f`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae10fbf74e9db38c4b611d58d3aabebe4336ef55f067d024a5753990d8ee0c65`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 485.0 KB (485022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b00a4239ecfe83a559cd5f40ff7a390b535f2c4a718c1dfcb11fb36e643bc6`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 6.4 MB (6381052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293d2ecab9ac866fa0d9cd648139d9576b12e77960c11dd976d1e874a69074e3`  
		Last Modified: Tue, 10 Dec 2024 23:29:18 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcaf4545aa895aefcb8f088f2fada2e81ed4f5ea5070c634da65a3226c5f454d`  
		Last Modified: Tue, 10 Dec 2024 23:29:18 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be99fe33f983eb453fe8c100eb4bc03e6d17392e701deae38cf0dcb416b86635`  
		Last Modified: Tue, 10 Dec 2024 23:29:18 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ace41bfa487712fd128caaa0b1ddb268f5cc6f198c990a822fa0b9a55c0cee7`  
		Last Modified: Tue, 10 Dec 2024 23:29:18 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:28de350897b589b46cbe9be25abd075eaad0faeb45ab4b1c832d1fa0dcf28d6d
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

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:1fd834581735b304465d440d706f668b245fa15c90864a8110d0069628504799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10017410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69bad2eb78b7ad191ae578a8cd1a90bb014cd770b959fdf75228696af9e957b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3eb8f37ad7a3d0e0d42022d3b399dbeb45f39b9a36dd95f9c74eb3ee4ff505`  
		Last Modified: Tue, 10 Dec 2024 23:27:27 GMT  
		Size: 6.4 MB (6371998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d30e571e9a33b90d53adc364b75dc4175a04f59de9d03895a30448068789fd`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64e4621359f08beab60eaf8e077f6f6ab0cec1ab6c999d1fdb4b35235662973`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:205d307881aedf2bd51cd9499b2e7cab47ada6b75a95df123216ad185b195a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9195c0eaed762824d5c53e56fe0b79a7d0d6375197aea07ffe383a513bb9a998`

```dockerfile
```

-	Layers:
	-	`sha256:069960ecffcdfc8e80d9352cfbe93b35fda077faf6c558950c05b3be76d07796`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:3569b3c6c6049c65c064d2c1638f58c6373d9779bfbafa529c82b117df449f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9387859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78fb87af3390f4d569e90248e5ef868c71ea224696608d9676420a21f08204f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d491d6ae32f791b6c6ee444da2433c3fe5f68f95a28a063e08fba789ebeb3f1`  
		Last Modified: Tue, 10 Dec 2024 23:27:13 GMT  
		Size: 6.0 MB (6019710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865e30e55f10109ec4fa649ff5598bb63785974f48e3467909963032f1b75bf3`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e27652e6cdf62ea6391042bda7e59583d83826301e119078799dc7674d5f916`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5c9032bdc8ef63d822723910e03076cf5c904847843dde7aa3597eb73c844ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4723e93aa61b1d00a73afea3fa2d282ca9b9cfbf288b20c9edb846ddc14746`

```dockerfile
```

-	Layers:
	-	`sha256:e07ee39720e7781ee4b9ccfe13bf58df6e7045efc1ed482c9f6a811ceb5c4cb0`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a0825f66cb5b9d7837459726ec6ca63a60b3888e8b67c655c7bd4c0ba05448cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9108253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9dd517c3a03af5824c23a81cedeed2598c4db1f301b3bc2e9bc40f4ab1bd618`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c84334747ecb5ce1375e80f91f5c140846eb6d7d51f9f6e6706641e1534c47`  
		Last Modified: Tue, 10 Dec 2024 23:27:11 GMT  
		Size: 6.0 MB (6007249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8010f8f3390c5e4323711c7f680070162d24e7fe3a14cf0e3d4670bd86647f9f`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573b54805f27aadae125876129ffbe488c10a85a15c36f50824d9ea4120537db`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6332c66401722e3837a6d186f7f9e1998a51350aa4b0af94507fbabb700ebb51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8a5df688f658118f4802867e4073818b174fd568574578a38138431bcbe412`

```dockerfile
```

-	Layers:
	-	`sha256:90edcaab6c14939090cda88a4bafbf0f09deddae7ca690ec3b1cda3e66db02a9`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:44905153cfe19be67e2baf248d1fe4a687aa2542e28efbff0f08f466e8749d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9912066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18b42869bfcbe5193535e39dc5571d303f0fcfd8c8fef4c6bb885ebe9b16b70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab592abba0f5f4ec119ae6d68f1206012d0485e97bb32949ec2a5bd04eb22f6`  
		Last Modified: Tue, 10 Dec 2024 23:27:05 GMT  
		Size: 5.9 MB (5917911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83961d61cdbd8298afd926b21e9e703be42edad95c17d626d5b2c8f8bdfafca`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403efcdcd91f4b94baeb36d579d722af0241889ee36afa8b92229b2c6eb937b4`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a25a621ca70ce2b0b97e30ce8ff0dbaed26cdf192d3a9f357bee0ee044c610d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850950126604011113cf97360a1b385355861ecabbe661483a1173cd8dd61172`

```dockerfile
```

-	Layers:
	-	`sha256:92f99c76a992a8785e402afdc8c8fee96331b60410b4a73baacc424b5d4ef722`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:d23003b22072b07cea7c57403d30519c9974445420181d8e174fbfa45fa533ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b0b23cf06fe3a7a78cbf9050f6de38b3cbd86fd9eadd9aa0b576d10af31480`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aaaa26dccaea10b5b83d01ed56f7a196c902179c89f7b031693a66884d17aef`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 5.7 MB (5738932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd34510b2845266284f593caae986bea90464fb438d79811c16c21afc268db9`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2beb0025099f5180f9671beb5f58c8b9fb8950f5971472ca2aded6d8c086dfcc`  
		Last Modified: Tue, 12 Nov 2024 03:03:02 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6ff0dd9b59f440e98ec6d6043cae3c81909695d9cf72e4f75ee2729e8104db86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72e08b6ff60c9977edbbe63a98b79f532617da8c1b3435d620244dd54347bea`

```dockerfile
```

-	Layers:
	-	`sha256:5f8a5a969359fee4a9f6bfec8cf77271b3a9243079c36ba7fbda1fadd5e0130c`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:d62285e97415380d73c75ff154d35fa1c6d6bec23a71995a671e665405d855b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9687191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658e5ca2d2437afce8173f52960e6280cfc673cd68edd78c9b60d8e50f94624b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f889b72b6e6f2f7a8f55853722d58f9f51fb766899e07465539676a22f0ca84`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 6.2 MB (6216702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995a4bc6424d4d94211f245dfd6f8f7975eea36b074521a866fbb75000ae79cd`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2990cf750e1e6ae965cb5ee3aa09fb5555f8709d7b9fd091ff70f124dd53a69d`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ef1002190acf6bcefe4da93459355df9b9bd492b52bf5895f710fadb82698c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bbee94701029b1f45fcbe9dbe8783e933466d45dd6eeefdb23d66cbb64483b5`

```dockerfile
```

-	Layers:
	-	`sha256:8c627f5f6e115176dd03af0a018e19fad71b8bb00277a4792730d383bd1e9868`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:alpine3.21`

```console
$ docker pull nats@sha256:87ed4c1ce118ac91e10e8b917c75085959d008a69219f32a0ddd3f31619b1adf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:1fd834581735b304465d440d706f668b245fa15c90864a8110d0069628504799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10017410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69bad2eb78b7ad191ae578a8cd1a90bb014cd770b959fdf75228696af9e957b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3eb8f37ad7a3d0e0d42022d3b399dbeb45f39b9a36dd95f9c74eb3ee4ff505`  
		Last Modified: Tue, 10 Dec 2024 23:27:27 GMT  
		Size: 6.4 MB (6371998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d30e571e9a33b90d53adc364b75dc4175a04f59de9d03895a30448068789fd`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64e4621359f08beab60eaf8e077f6f6ab0cec1ab6c999d1fdb4b35235662973`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:205d307881aedf2bd51cd9499b2e7cab47ada6b75a95df123216ad185b195a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9195c0eaed762824d5c53e56fe0b79a7d0d6375197aea07ffe383a513bb9a998`

```dockerfile
```

-	Layers:
	-	`sha256:069960ecffcdfc8e80d9352cfbe93b35fda077faf6c558950c05b3be76d07796`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:3569b3c6c6049c65c064d2c1638f58c6373d9779bfbafa529c82b117df449f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9387859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78fb87af3390f4d569e90248e5ef868c71ea224696608d9676420a21f08204f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d491d6ae32f791b6c6ee444da2433c3fe5f68f95a28a063e08fba789ebeb3f1`  
		Last Modified: Tue, 10 Dec 2024 23:27:13 GMT  
		Size: 6.0 MB (6019710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865e30e55f10109ec4fa649ff5598bb63785974f48e3467909963032f1b75bf3`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e27652e6cdf62ea6391042bda7e59583d83826301e119078799dc7674d5f916`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:5c9032bdc8ef63d822723910e03076cf5c904847843dde7aa3597eb73c844ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4723e93aa61b1d00a73afea3fa2d282ca9b9cfbf288b20c9edb846ddc14746`

```dockerfile
```

-	Layers:
	-	`sha256:e07ee39720e7781ee4b9ccfe13bf58df6e7045efc1ed482c9f6a811ceb5c4cb0`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:a0825f66cb5b9d7837459726ec6ca63a60b3888e8b67c655c7bd4c0ba05448cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9108253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9dd517c3a03af5824c23a81cedeed2598c4db1f301b3bc2e9bc40f4ab1bd618`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c84334747ecb5ce1375e80f91f5c140846eb6d7d51f9f6e6706641e1534c47`  
		Last Modified: Tue, 10 Dec 2024 23:27:11 GMT  
		Size: 6.0 MB (6007249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8010f8f3390c5e4323711c7f680070162d24e7fe3a14cf0e3d4670bd86647f9f`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573b54805f27aadae125876129ffbe488c10a85a15c36f50824d9ea4120537db`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:6332c66401722e3837a6d186f7f9e1998a51350aa4b0af94507fbabb700ebb51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8a5df688f658118f4802867e4073818b174fd568574578a38138431bcbe412`

```dockerfile
```

-	Layers:
	-	`sha256:90edcaab6c14939090cda88a4bafbf0f09deddae7ca690ec3b1cda3e66db02a9`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:44905153cfe19be67e2baf248d1fe4a687aa2542e28efbff0f08f466e8749d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9912066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18b42869bfcbe5193535e39dc5571d303f0fcfd8c8fef4c6bb885ebe9b16b70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab592abba0f5f4ec119ae6d68f1206012d0485e97bb32949ec2a5bd04eb22f6`  
		Last Modified: Tue, 10 Dec 2024 23:27:05 GMT  
		Size: 5.9 MB (5917911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83961d61cdbd8298afd926b21e9e703be42edad95c17d626d5b2c8f8bdfafca`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403efcdcd91f4b94baeb36d579d722af0241889ee36afa8b92229b2c6eb937b4`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:a25a621ca70ce2b0b97e30ce8ff0dbaed26cdf192d3a9f357bee0ee044c610d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850950126604011113cf97360a1b385355861ecabbe661483a1173cd8dd61172`

```dockerfile
```

-	Layers:
	-	`sha256:92f99c76a992a8785e402afdc8c8fee96331b60410b4a73baacc424b5d4ef722`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:d62285e97415380d73c75ff154d35fa1c6d6bec23a71995a671e665405d855b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9687191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658e5ca2d2437afce8173f52960e6280cfc673cd68edd78c9b60d8e50f94624b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f889b72b6e6f2f7a8f55853722d58f9f51fb766899e07465539676a22f0ca84`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 6.2 MB (6216702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995a4bc6424d4d94211f245dfd6f8f7975eea36b074521a866fbb75000ae79cd`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2990cf750e1e6ae965cb5ee3aa09fb5555f8709d7b9fd091ff70f124dd53a69d`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:ef1002190acf6bcefe4da93459355df9b9bd492b52bf5895f710fadb82698c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bbee94701029b1f45fcbe9dbe8783e933466d45dd6eeefdb23d66cbb64483b5`

```dockerfile
```

-	Layers:
	-	`sha256:8c627f5f6e115176dd03af0a018e19fad71b8bb00277a4792730d383bd1e9868`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:latest`

```console
$ docker pull nats@sha256:d15749dc10d8e67b55f496551ca3794b2f131556342b313eb3e6115ec75f6fb3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
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
	-	windows version 10.0.17763.6532; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:26b0ee1a95285aedae137aefb953701d9da1dfffcf7818eb3aeb536c4373892f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9321c727224d6919153399a2554913ee3ea75615c40faf0b0b61719fd4cba18f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc7b6eeb42db27589fb02b7af7648621b4230b391664f1cabca731c0cb74c6c0`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.7 MB (5748809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648a1fe081b19052a39d36fde23ff89c48a0b60bddc52cdf58474ed9b7e16ab4`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:92b63acf1eb46cb3ce90a6406fcf9cf3214ba330e4dacef512280529a04870ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd7260fa709b7a3bb731d03f1fc89313f81c37eaacc9a95aef394dde1aa26ae`

```dockerfile
```

-	Layers:
	-	`sha256:eb1f99c4d9cf8c2d861e264c9ba0cdb9161bb70c2764c955ab1f90310af1f472`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:ed0d3d3f325c395d64fe3cce644fcb8a85dd7f693321155adc742f9a4558a524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5414498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb43c0fb21e266dce12015b728c78e144c79b548aa91729dffae13470e0d9297`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:359939d6b9b0e79cd20ca9621811c48e03c3d4a5b7af0a099486d520bf5d7b5f`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.4 MB (5413989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f789fb3e9d2d0ff4362d663dece6c6656816327c3c477f706bb39361ec1cd75`  
		Last Modified: Tue, 12 Nov 2024 15:37:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:6ed1504d0cb0d9a7e50ccb85fa202b5d8901dc4bc331ec9212598e39c7cb9708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35958b08d07b59577364ce756c66f53782d4b469b1eb5fa49f8e1d5b54cdca4`

```dockerfile
```

-	Layers:
	-	`sha256:4666424ba74b452fb83d3ee0779517652e5b5c382cd17ac41b3a6eed5fa553c9`  
		Last Modified: Tue, 12 Nov 2024 15:37:52 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:6e124d1272a57524b4ca6d20f067a1bcaaf0698436552c1e023098e8d86f3ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5402382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48a99f0a97426e5e74f3a25a607b2c16d9a4521a32a2ba12fa6fdd0202e4bf5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d05d846e8109608ff47e05c22bb31057b6b6430dcabb8110890869d111bd1b9e`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.4 MB (5401872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2f51350cd72f7f51dbac3739d56b990a14dbbf86618c4893c441ddc4b1bb8c`  
		Last Modified: Wed, 13 Nov 2024 06:50:55 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:8961a748bcb9e725a669f8fa2f9feb42d333982353b703fc2ab7d1dcc75672df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f520b399deef237b5cb2d8124b151ec2c5226e54324dd079da79164fb174dba`

```dockerfile
```

-	Layers:
	-	`sha256:1eee6a8956b4ad976df210a755d0ef0e99d56f92ba24d749b7da0611fad96580`  
		Last Modified: Wed, 13 Nov 2024 06:50:55 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a472fd5123d4894808a5300ae620b1fc75173683a27bef46da8f72cffc933c98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5311420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b2641c24dab528ab7f50965ba60bf552fd0741d08bce6d7eb119bdb14c2eb9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:38a1a08cf356fa2c344f9efdd2f487176ba47d86dbe408ea24116528e7638b79`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.3 MB (5310912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f500aab43d6d7fb9af41817fd3e6d15af8d2cea39f195b594bb2aaf7ea3f8a3e`  
		Last Modified: Wed, 13 Nov 2024 01:53:01 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:28b2143fc08c4b9fa3086b9adbeb584e61f0fd522723dab3544ba1cf8d69f896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b61c129357d5acdec05b9878360c584d3e152bff6203d60fb73bba1d793c8f`

```dockerfile
```

-	Layers:
	-	`sha256:4292e75d9c32bf0ba80c2339d71516e065e70a4058f12e0d895837e96fa29963`  
		Last Modified: Wed, 13 Nov 2024 01:53:01 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:bfc123cdde6254307ee92ec40bfec41601825fb47a75326b4360f44bab372a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe22c4f1bea64db8b0f24a64002aa2061b73145c74e4218b813d0639491ea37`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:76bf2b5924879fa33a4c81c16fab61afb5d237715cb64ef9e8847f5b8cd91151`  
		Last Modified: Thu, 17 Oct 2024 18:09:44 GMT  
		Size: 5.3 MB (5279091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22806de38895554cf572cdc72c340ce1c2a1e339ea920a8fd272f6908805d555`  
		Last Modified: Tue, 12 Nov 2024 15:01:33 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:c68e4834537eedd18677a7ba9c608218c21721b078d08969c0d9c47a48e5a2bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6620d942923f41e16c63215620c4590dade6c160c8b3464748128fc3f4fe9f1`

```dockerfile
```

-	Layers:
	-	`sha256:f936acbf9b3ac4e546df2f3f5b7c04867dfd20bc3b0efd62c5b655a66d588f46`  
		Last Modified: Tue, 12 Nov 2024 15:01:33 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:860ac3f0cce933e2518b5dfad7e4ceb5d0a65e5e4958848ea12f0e2cf6262e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b1957d328a071a836284d4b15fee34cc4d49960896e4f141a5d8ff677d654e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fffb3288c2f56b83007e69c7219ef513ffc8b9f7f218885669a4d81f7aea10c7`  
		Last Modified: Thu, 17 Oct 2024 18:09:45 GMT  
		Size: 5.6 MB (5603688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2fd1adb449a2e37ee7766e0822200ce9fef4742f0a63f4271d9db4b8e2f3f1`  
		Last Modified: Tue, 12 Nov 2024 22:35:30 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:0f6e8d82de7f4a5a2d5fc517757ceaf8a2a1411abfc8fdc89d44e7a32f7c1ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67bf5d4378b516209f4da80c21451bb69cbb934cf3b8d37e72dfbab1a5bb6c44`

```dockerfile
```

-	Layers:
	-	`sha256:236407df6864bbf886cc676be754b255160b1a1aece15f8331b5062b41bc981e`  
		Last Modified: Tue, 12 Nov 2024 22:35:30 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:af099d0ad09f68427f6716cbe03227c5409000f9021c92a4981a6099e9901dc7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161090154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e23925b656567c9ef8ee2bc478e0ada3269421cc962f905108b7ac70bfc5d2f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Thu, 14 Nov 2024 21:26:06 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 14 Nov 2024 21:26:11 GMT
RUN cmd /S /C #(nop) COPY file:6efa011ff84014d148ada9315a3292149a71c3daa1b536499f2b43a2daee2d50 in C:\nats-server.exe 
# Thu, 14 Nov 2024 21:26:12 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Nov 2024 21:26:12 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 14 Nov 2024 21:26:13 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Nov 2024 21:26:14 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077c935cc00e1acf8d3769c81d23f3134507c1149593f2af1de160f98fd769e3`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb87536f0d2cb71d86892dcf0a7036c92d682cdf7e3a8dadda31d9569a62118`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 5.9 MB (5870083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929a1f4fa9be7e6e28a451ae8e437938d70bb70ab75539f175ac46be518d2292`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d64f781d33814e56a5a3e633b6778e34fb06d03ee0cf92a7b1931ffea43af5`  
		Last Modified: Thu, 14 Nov 2024 21:26:16 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f881ff7235bc92d60a608d0336719df84a7f2a45c17ef58277f678e69e3acb1b`  
		Last Modified: Thu, 14 Nov 2024 21:26:16 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d5e5b49ab6c4788712962e67498e176b4fdb803f692b97a96580ca87f612c`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:23638865a8c200681a3a58ee86cd9c5776bbc7499f5525ce9c9baae4d4970d2a
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

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:26b0ee1a95285aedae137aefb953701d9da1dfffcf7818eb3aeb536c4373892f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9321c727224d6919153399a2554913ee3ea75615c40faf0b0b61719fd4cba18f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc7b6eeb42db27589fb02b7af7648621b4230b391664f1cabca731c0cb74c6c0`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.7 MB (5748809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648a1fe081b19052a39d36fde23ff89c48a0b60bddc52cdf58474ed9b7e16ab4`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:92b63acf1eb46cb3ce90a6406fcf9cf3214ba330e4dacef512280529a04870ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd7260fa709b7a3bb731d03f1fc89313f81c37eaacc9a95aef394dde1aa26ae`

```dockerfile
```

-	Layers:
	-	`sha256:eb1f99c4d9cf8c2d861e264c9ba0cdb9161bb70c2764c955ab1f90310af1f472`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:ed0d3d3f325c395d64fe3cce644fcb8a85dd7f693321155adc742f9a4558a524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5414498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb43c0fb21e266dce12015b728c78e144c79b548aa91729dffae13470e0d9297`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:359939d6b9b0e79cd20ca9621811c48e03c3d4a5b7af0a099486d520bf5d7b5f`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.4 MB (5413989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f789fb3e9d2d0ff4362d663dece6c6656816327c3c477f706bb39361ec1cd75`  
		Last Modified: Tue, 12 Nov 2024 15:37:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:6ed1504d0cb0d9a7e50ccb85fa202b5d8901dc4bc331ec9212598e39c7cb9708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35958b08d07b59577364ce756c66f53782d4b469b1eb5fa49f8e1d5b54cdca4`

```dockerfile
```

-	Layers:
	-	`sha256:4666424ba74b452fb83d3ee0779517652e5b5c382cd17ac41b3a6eed5fa553c9`  
		Last Modified: Tue, 12 Nov 2024 15:37:52 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:6e124d1272a57524b4ca6d20f067a1bcaaf0698436552c1e023098e8d86f3ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5402382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48a99f0a97426e5e74f3a25a607b2c16d9a4521a32a2ba12fa6fdd0202e4bf5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d05d846e8109608ff47e05c22bb31057b6b6430dcabb8110890869d111bd1b9e`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.4 MB (5401872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2f51350cd72f7f51dbac3739d56b990a14dbbf86618c4893c441ddc4b1bb8c`  
		Last Modified: Wed, 13 Nov 2024 06:50:55 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:8961a748bcb9e725a669f8fa2f9feb42d333982353b703fc2ab7d1dcc75672df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f520b399deef237b5cb2d8124b151ec2c5226e54324dd079da79164fb174dba`

```dockerfile
```

-	Layers:
	-	`sha256:1eee6a8956b4ad976df210a755d0ef0e99d56f92ba24d749b7da0611fad96580`  
		Last Modified: Wed, 13 Nov 2024 06:50:55 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a472fd5123d4894808a5300ae620b1fc75173683a27bef46da8f72cffc933c98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5311420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b2641c24dab528ab7f50965ba60bf552fd0741d08bce6d7eb119bdb14c2eb9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:38a1a08cf356fa2c344f9efdd2f487176ba47d86dbe408ea24116528e7638b79`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.3 MB (5310912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f500aab43d6d7fb9af41817fd3e6d15af8d2cea39f195b594bb2aaf7ea3f8a3e`  
		Last Modified: Wed, 13 Nov 2024 01:53:01 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:28b2143fc08c4b9fa3086b9adbeb584e61f0fd522723dab3544ba1cf8d69f896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b61c129357d5acdec05b9878360c584d3e152bff6203d60fb73bba1d793c8f`

```dockerfile
```

-	Layers:
	-	`sha256:4292e75d9c32bf0ba80c2339d71516e065e70a4058f12e0d895837e96fa29963`  
		Last Modified: Wed, 13 Nov 2024 01:53:01 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:bfc123cdde6254307ee92ec40bfec41601825fb47a75326b4360f44bab372a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe22c4f1bea64db8b0f24a64002aa2061b73145c74e4218b813d0639491ea37`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:76bf2b5924879fa33a4c81c16fab61afb5d237715cb64ef9e8847f5b8cd91151`  
		Last Modified: Thu, 17 Oct 2024 18:09:44 GMT  
		Size: 5.3 MB (5279091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22806de38895554cf572cdc72c340ce1c2a1e339ea920a8fd272f6908805d555`  
		Last Modified: Tue, 12 Nov 2024 15:01:33 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:c68e4834537eedd18677a7ba9c608218c21721b078d08969c0d9c47a48e5a2bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6620d942923f41e16c63215620c4590dade6c160c8b3464748128fc3f4fe9f1`

```dockerfile
```

-	Layers:
	-	`sha256:f936acbf9b3ac4e546df2f3f5b7c04867dfd20bc3b0efd62c5b655a66d588f46`  
		Last Modified: Tue, 12 Nov 2024 15:01:33 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:860ac3f0cce933e2518b5dfad7e4ceb5d0a65e5e4958848ea12f0e2cf6262e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b1957d328a071a836284d4b15fee34cc4d49960896e4f141a5d8ff677d654e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fffb3288c2f56b83007e69c7219ef513ffc8b9f7f218885669a4d81f7aea10c7`  
		Last Modified: Thu, 17 Oct 2024 18:09:45 GMT  
		Size: 5.6 MB (5603688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2fd1adb449a2e37ee7766e0822200ce9fef4742f0a63f4271d9db4b8e2f3f1`  
		Last Modified: Tue, 12 Nov 2024 22:35:30 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:0f6e8d82de7f4a5a2d5fc517757ceaf8a2a1411abfc8fdc89d44e7a32f7c1ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67bf5d4378b516209f4da80c21451bb69cbb934cf3b8d37e72dfbab1a5bb6c44`

```dockerfile
```

-	Layers:
	-	`sha256:236407df6864bbf886cc676be754b255160b1a1aece15f8331b5062b41bc981e`  
		Last Modified: Tue, 12 Nov 2024 22:35:30 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:nanoserver`

```console
$ docker pull nats@sha256:070f9e269bf92f0bedac63b5a0f269f7520ad54e071f7953b5c35621160ad025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `nats:nanoserver` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:af099d0ad09f68427f6716cbe03227c5409000f9021c92a4981a6099e9901dc7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161090154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e23925b656567c9ef8ee2bc478e0ada3269421cc962f905108b7ac70bfc5d2f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Thu, 14 Nov 2024 21:26:06 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 14 Nov 2024 21:26:11 GMT
RUN cmd /S /C #(nop) COPY file:6efa011ff84014d148ada9315a3292149a71c3daa1b536499f2b43a2daee2d50 in C:\nats-server.exe 
# Thu, 14 Nov 2024 21:26:12 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Nov 2024 21:26:12 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 14 Nov 2024 21:26:13 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Nov 2024 21:26:14 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077c935cc00e1acf8d3769c81d23f3134507c1149593f2af1de160f98fd769e3`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb87536f0d2cb71d86892dcf0a7036c92d682cdf7e3a8dadda31d9569a62118`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 5.9 MB (5870083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929a1f4fa9be7e6e28a451ae8e437938d70bb70ab75539f175ac46be518d2292`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d64f781d33814e56a5a3e633b6778e34fb06d03ee0cf92a7b1931ffea43af5`  
		Last Modified: Thu, 14 Nov 2024 21:26:16 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f881ff7235bc92d60a608d0336719df84a7f2a45c17ef58277f678e69e3acb1b`  
		Last Modified: Thu, 14 Nov 2024 21:26:16 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d5e5b49ab6c4788712962e67498e176b4fdb803f692b97a96580ca87f612c`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:070f9e269bf92f0bedac63b5a0f269f7520ad54e071f7953b5c35621160ad025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:af099d0ad09f68427f6716cbe03227c5409000f9021c92a4981a6099e9901dc7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161090154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e23925b656567c9ef8ee2bc478e0ada3269421cc962f905108b7ac70bfc5d2f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Thu, 14 Nov 2024 21:26:06 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 14 Nov 2024 21:26:11 GMT
RUN cmd /S /C #(nop) COPY file:6efa011ff84014d148ada9315a3292149a71c3daa1b536499f2b43a2daee2d50 in C:\nats-server.exe 
# Thu, 14 Nov 2024 21:26:12 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Nov 2024 21:26:12 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 14 Nov 2024 21:26:13 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Nov 2024 21:26:14 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077c935cc00e1acf8d3769c81d23f3134507c1149593f2af1de160f98fd769e3`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb87536f0d2cb71d86892dcf0a7036c92d682cdf7e3a8dadda31d9569a62118`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 5.9 MB (5870083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929a1f4fa9be7e6e28a451ae8e437938d70bb70ab75539f175ac46be518d2292`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d64f781d33814e56a5a3e633b6778e34fb06d03ee0cf92a7b1931ffea43af5`  
		Last Modified: Thu, 14 Nov 2024 21:26:16 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f881ff7235bc92d60a608d0336719df84a7f2a45c17ef58277f678e69e3acb1b`  
		Last Modified: Thu, 14 Nov 2024 21:26:16 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d5e5b49ab6c4788712962e67498e176b4fdb803f692b97a96580ca87f612c`  
		Last Modified: Thu, 14 Nov 2024 21:26:17 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:23638865a8c200681a3a58ee86cd9c5776bbc7499f5525ce9c9baae4d4970d2a
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
$ docker pull nats@sha256:26b0ee1a95285aedae137aefb953701d9da1dfffcf7818eb3aeb536c4373892f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9321c727224d6919153399a2554913ee3ea75615c40faf0b0b61719fd4cba18f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc7b6eeb42db27589fb02b7af7648621b4230b391664f1cabca731c0cb74c6c0`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.7 MB (5748809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648a1fe081b19052a39d36fde23ff89c48a0b60bddc52cdf58474ed9b7e16ab4`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:92b63acf1eb46cb3ce90a6406fcf9cf3214ba330e4dacef512280529a04870ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd7260fa709b7a3bb731d03f1fc89313f81c37eaacc9a95aef394dde1aa26ae`

```dockerfile
```

-	Layers:
	-	`sha256:eb1f99c4d9cf8c2d861e264c9ba0cdb9161bb70c2764c955ab1f90310af1f472`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:ed0d3d3f325c395d64fe3cce644fcb8a85dd7f693321155adc742f9a4558a524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5414498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb43c0fb21e266dce12015b728c78e144c79b548aa91729dffae13470e0d9297`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:359939d6b9b0e79cd20ca9621811c48e03c3d4a5b7af0a099486d520bf5d7b5f`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.4 MB (5413989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f789fb3e9d2d0ff4362d663dece6c6656816327c3c477f706bb39361ec1cd75`  
		Last Modified: Tue, 12 Nov 2024 15:37:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:6ed1504d0cb0d9a7e50ccb85fa202b5d8901dc4bc331ec9212598e39c7cb9708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35958b08d07b59577364ce756c66f53782d4b469b1eb5fa49f8e1d5b54cdca4`

```dockerfile
```

-	Layers:
	-	`sha256:4666424ba74b452fb83d3ee0779517652e5b5c382cd17ac41b3a6eed5fa553c9`  
		Last Modified: Tue, 12 Nov 2024 15:37:52 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:6e124d1272a57524b4ca6d20f067a1bcaaf0698436552c1e023098e8d86f3ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5402382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48a99f0a97426e5e74f3a25a607b2c16d9a4521a32a2ba12fa6fdd0202e4bf5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d05d846e8109608ff47e05c22bb31057b6b6430dcabb8110890869d111bd1b9e`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.4 MB (5401872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2f51350cd72f7f51dbac3739d56b990a14dbbf86618c4893c441ddc4b1bb8c`  
		Last Modified: Wed, 13 Nov 2024 06:50:55 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:8961a748bcb9e725a669f8fa2f9feb42d333982353b703fc2ab7d1dcc75672df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f520b399deef237b5cb2d8124b151ec2c5226e54324dd079da79164fb174dba`

```dockerfile
```

-	Layers:
	-	`sha256:1eee6a8956b4ad976df210a755d0ef0e99d56f92ba24d749b7da0611fad96580`  
		Last Modified: Wed, 13 Nov 2024 06:50:55 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a472fd5123d4894808a5300ae620b1fc75173683a27bef46da8f72cffc933c98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5311420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b2641c24dab528ab7f50965ba60bf552fd0741d08bce6d7eb119bdb14c2eb9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:38a1a08cf356fa2c344f9efdd2f487176ba47d86dbe408ea24116528e7638b79`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.3 MB (5310912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f500aab43d6d7fb9af41817fd3e6d15af8d2cea39f195b594bb2aaf7ea3f8a3e`  
		Last Modified: Wed, 13 Nov 2024 01:53:01 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:28b2143fc08c4b9fa3086b9adbeb584e61f0fd522723dab3544ba1cf8d69f896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b61c129357d5acdec05b9878360c584d3e152bff6203d60fb73bba1d793c8f`

```dockerfile
```

-	Layers:
	-	`sha256:4292e75d9c32bf0ba80c2339d71516e065e70a4058f12e0d895837e96fa29963`  
		Last Modified: Wed, 13 Nov 2024 01:53:01 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:bfc123cdde6254307ee92ec40bfec41601825fb47a75326b4360f44bab372a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe22c4f1bea64db8b0f24a64002aa2061b73145c74e4218b813d0639491ea37`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:76bf2b5924879fa33a4c81c16fab61afb5d237715cb64ef9e8847f5b8cd91151`  
		Last Modified: Thu, 17 Oct 2024 18:09:44 GMT  
		Size: 5.3 MB (5279091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22806de38895554cf572cdc72c340ce1c2a1e339ea920a8fd272f6908805d555`  
		Last Modified: Tue, 12 Nov 2024 15:01:33 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:c68e4834537eedd18677a7ba9c608218c21721b078d08969c0d9c47a48e5a2bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6620d942923f41e16c63215620c4590dade6c160c8b3464748128fc3f4fe9f1`

```dockerfile
```

-	Layers:
	-	`sha256:f936acbf9b3ac4e546df2f3f5b7c04867dfd20bc3b0efd62c5b655a66d588f46`  
		Last Modified: Tue, 12 Nov 2024 15:01:33 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:860ac3f0cce933e2518b5dfad7e4ceb5d0a65e5e4958848ea12f0e2cf6262e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b1957d328a071a836284d4b15fee34cc4d49960896e4f141a5d8ff677d654e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fffb3288c2f56b83007e69c7219ef513ffc8b9f7f218885669a4d81f7aea10c7`  
		Last Modified: Thu, 17 Oct 2024 18:09:45 GMT  
		Size: 5.6 MB (5603688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2fd1adb449a2e37ee7766e0822200ce9fef4742f0a63f4271d9db4b8e2f3f1`  
		Last Modified: Tue, 12 Nov 2024 22:35:30 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:0f6e8d82de7f4a5a2d5fc517757ceaf8a2a1411abfc8fdc89d44e7a32f7c1ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67bf5d4378b516209f4da80c21451bb69cbb934cf3b8d37e72dfbab1a5bb6c44`

```dockerfile
```

-	Layers:
	-	`sha256:236407df6864bbf886cc676be754b255160b1a1aece15f8331b5062b41bc981e`  
		Last Modified: Tue, 12 Nov 2024 22:35:30 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:43fbcf8dfa35b4760178e0b4e16c2474d68f1ab3128b980817133057582d7e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `nats:windowsservercore` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:d8404f289d887ce07c6ec8c2ed3f2512727f6d6d33791e6f0d607f03a7bb99d0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2017532110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91991216a6a1544d8f469907d8e4e7e7aeb83722aa7f22591fb24566360cc0ab`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Tue, 10 Dec 2024 23:27:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Dec 2024 23:27:31 GMT
ENV NATS_DOCKERIZED=1
# Tue, 10 Dec 2024 23:27:32 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 23:27:32 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.23/nats-server-v2.10.23-windows-amd64.zip
# Tue, 10 Dec 2024 23:27:33 GMT
ENV NATS_SERVER_SHASUM=4ec39c0df08823a062dcdaac23ccf7ee56e76ccc27b69134f3e9b1549bc0f305
# Tue, 10 Dec 2024 23:28:50 GMT
RUN Set-PSDebug -Trace 2
# Tue, 10 Dec 2024 23:29:14 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 10 Dec 2024 23:29:14 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 10 Dec 2024 23:29:15 GMT
EXPOSE 4222 6222 8222
# Tue, 10 Dec 2024 23:29:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Dec 2024 23:29:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05963517ca3d5c411c11e9cf4ac529f3affa194a7f0914374d3b98008e19fcd`  
		Last Modified: Tue, 10 Dec 2024 23:29:20 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d8577eb6f25bb0f27f3d64f76584102e62ec7d909b34960f3f37f832653a0e`  
		Last Modified: Tue, 10 Dec 2024 23:29:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d70b39f16077baba91f50f30b3e69fbb08e38919da455c6ab5aad8d102b0a4`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231308f503d04392a55f1811db0102c1873660ab3780d766220170f78845628d`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8454af0dc55c7414c29902b1ae692d77206dbf2d5e0329ea7f4d00b32e43981f`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae10fbf74e9db38c4b611d58d3aabebe4336ef55f067d024a5753990d8ee0c65`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 485.0 KB (485022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b00a4239ecfe83a559cd5f40ff7a390b535f2c4a718c1dfcb11fb36e643bc6`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 6.4 MB (6381052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293d2ecab9ac866fa0d9cd648139d9576b12e77960c11dd976d1e874a69074e3`  
		Last Modified: Tue, 10 Dec 2024 23:29:18 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcaf4545aa895aefcb8f088f2fada2e81ed4f5ea5070c634da65a3226c5f454d`  
		Last Modified: Tue, 10 Dec 2024 23:29:18 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be99fe33f983eb453fe8c100eb4bc03e6d17392e701deae38cf0dcb416b86635`  
		Last Modified: Tue, 10 Dec 2024 23:29:18 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ace41bfa487712fd128caaa0b1ddb268f5cc6f198c990a822fa0b9a55c0cee7`  
		Last Modified: Tue, 10 Dec 2024 23:29:18 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:43fbcf8dfa35b4760178e0b4e16c2474d68f1ab3128b980817133057582d7e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:d8404f289d887ce07c6ec8c2ed3f2512727f6d6d33791e6f0d607f03a7bb99d0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2017532110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91991216a6a1544d8f469907d8e4e7e7aeb83722aa7f22591fb24566360cc0ab`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Tue, 10 Dec 2024 23:27:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Dec 2024 23:27:31 GMT
ENV NATS_DOCKERIZED=1
# Tue, 10 Dec 2024 23:27:32 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 23:27:32 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.23/nats-server-v2.10.23-windows-amd64.zip
# Tue, 10 Dec 2024 23:27:33 GMT
ENV NATS_SERVER_SHASUM=4ec39c0df08823a062dcdaac23ccf7ee56e76ccc27b69134f3e9b1549bc0f305
# Tue, 10 Dec 2024 23:28:50 GMT
RUN Set-PSDebug -Trace 2
# Tue, 10 Dec 2024 23:29:14 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 10 Dec 2024 23:29:14 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 10 Dec 2024 23:29:15 GMT
EXPOSE 4222 6222 8222
# Tue, 10 Dec 2024 23:29:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Dec 2024 23:29:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05963517ca3d5c411c11e9cf4ac529f3affa194a7f0914374d3b98008e19fcd`  
		Last Modified: Tue, 10 Dec 2024 23:29:20 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d8577eb6f25bb0f27f3d64f76584102e62ec7d909b34960f3f37f832653a0e`  
		Last Modified: Tue, 10 Dec 2024 23:29:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d70b39f16077baba91f50f30b3e69fbb08e38919da455c6ab5aad8d102b0a4`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231308f503d04392a55f1811db0102c1873660ab3780d766220170f78845628d`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8454af0dc55c7414c29902b1ae692d77206dbf2d5e0329ea7f4d00b32e43981f`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae10fbf74e9db38c4b611d58d3aabebe4336ef55f067d024a5753990d8ee0c65`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 485.0 KB (485022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b00a4239ecfe83a559cd5f40ff7a390b535f2c4a718c1dfcb11fb36e643bc6`  
		Last Modified: Tue, 10 Dec 2024 23:29:19 GMT  
		Size: 6.4 MB (6381052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293d2ecab9ac866fa0d9cd648139d9576b12e77960c11dd976d1e874a69074e3`  
		Last Modified: Tue, 10 Dec 2024 23:29:18 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcaf4545aa895aefcb8f088f2fada2e81ed4f5ea5070c634da65a3226c5f454d`  
		Last Modified: Tue, 10 Dec 2024 23:29:18 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be99fe33f983eb453fe8c100eb4bc03e6d17392e701deae38cf0dcb416b86635`  
		Last Modified: Tue, 10 Dec 2024 23:29:18 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ace41bfa487712fd128caaa0b1ddb268f5cc6f198c990a822fa0b9a55c0cee7`  
		Last Modified: Tue, 10 Dec 2024 23:29:18 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
