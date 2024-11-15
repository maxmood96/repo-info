<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.20`](#nats2-alpine320)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2.10`](#nats210)
-	[`nats:2.10-alpine`](#nats210-alpine)
-	[`nats:2.10-alpine3.20`](#nats210-alpine320)
-	[`nats:2.10-linux`](#nats210-linux)
-	[`nats:2.10-nanoserver`](#nats210-nanoserver)
-	[`nats:2.10-nanoserver-1809`](#nats210-nanoserver-1809)
-	[`nats:2.10-scratch`](#nats210-scratch)
-	[`nats:2.10-windowsservercore`](#nats210-windowsservercore)
-	[`nats:2.10-windowsservercore-1809`](#nats210-windowsservercore-1809)
-	[`nats:2.10.22`](#nats21022)
-	[`nats:2.10.22-alpine`](#nats21022-alpine)
-	[`nats:2.10.22-alpine3.20`](#nats21022-alpine320)
-	[`nats:2.10.22-linux`](#nats21022-linux)
-	[`nats:2.10.22-nanoserver`](#nats21022-nanoserver)
-	[`nats:2.10.22-nanoserver-1809`](#nats21022-nanoserver-1809)
-	[`nats:2.10.22-scratch`](#nats21022-scratch)
-	[`nats:2.10.22-windowsservercore`](#nats21022-windowsservercore)
-	[`nats:2.10.22-windowsservercore-1809`](#nats21022-windowsservercore-1809)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.20`](#natsalpine320)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)

## `nats:2`

```console
$ docker pull nats@sha256:6658c4197669a20542109153a783caccc2642eecd007a491467aeb684d6c1ac0
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
	-	windows version 10.0.17763.6414; amd64

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

### `nats:2` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:053fd6a67430966b5ef4253d8b1cfc23a311da729a9389d83b3dfd01800e63ce
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842d20e36f047cfb078828de10ee4d9abbbd7eebde56d0c84f6d90843adee82a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Tue, 12 Nov 2024 02:02:48 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Nov 2024 02:02:49 GMT
RUN cmd /S /C #(nop) COPY file:6efa011ff84014d148ada9315a3292149a71c3daa1b536499f2b43a2daee2d50 in C:\nats-server.exe 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3c2d0f66b6ae0af6bb08b99b128223baab674d525e452e0991867c2a1173b0`  
		Last Modified: Tue, 12 Nov 2024 02:02:57 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ba4c6aafec94bd41860c1d9e8327b73b0ac64c85b1c317350f3df49318178d`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 5.9 MB (5870082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af1e1e6a4962ecc81604ad1b09ea03a4519d9de02bfd8f36edb94d3f8bef32`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1db4ff41e188b9274e333b99fd768fd30e9023a68547ce0a4f7f910f0e3e88`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c3ee6788b430468c453082a98238ebe894e2beb7699b2dc742b1e842ed0616`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619838cdeb9173ba7f68fc27c3eaf3bbd6cb680b441c766e7f4274f6b25573f6`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:73b0ba5fec5518c5f698597c58d2a3350a2b5ccae43e84c308f8d2da1242deca
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
$ docker pull nats@sha256:aa536352f09b109b909e8bfbf9859a40601481bb3742ebc7a09cfaf638622407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ede291869d412212887b120efa5c8b7f3b08aefea8f280cd067254c01c2821e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d773e5a5acd4a5185e1795ce442fae0815b4cde8653279c82cb254f75c731910`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 6.2 MB (6205667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae6cea471c207a94e7b03500b522e43c2a3eadd03542e610de9d99ab66afb0`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae68805e7e9a1127a5a8d98e4da64d38cf8b0d9bd426df532b489f42860fd6ea`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:02807cf2f8c136dbf08462f9e4830c0ebe9789135bd35f9dc1b3bed84498f403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7502fcca317f6d32816fbedbe1b62bc47f8c999075143f1668fe57bce064a8`

```dockerfile
```

-	Layers:
	-	`sha256:2d235c7a9ec1b8f79a5b506d4f47baa00cda2f90ab4c8e3e4b95135a10c82667`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:08995147ec70b3d9cf6231fcaf9c5693f13f0f8fd2350e601c621f38b84d6e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9237219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d69a74357f1c0cc0b96cfa8306847367e64f3404a70a674e10549211ca3787`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
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
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65afc62adacdff0bf527d9f1b6aaf695b5d37e83fe01a9318f61f316f7f181b6`  
		Last Modified: Tue, 12 Nov 2024 02:43:39 GMT  
		Size: 5.9 MB (5869651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970e0190e0f471373e9e66c70a2752250ed9e69da363c0bfba42143fede6fdf1`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191dbad2f5874fb9d2a78809f1cb2d73967711a343f8a69c0d2feaae390b4b80`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f9d6d9aa5070fd9051dc1f6b9b181fb2d58de8807e51d6258c1f350ab3b25b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815d234991f683d0c7e6bf47ad52a53158e360aad37d3918ef50be115c7513f7`

```dockerfile
```

-	Layers:
	-	`sha256:4c385d33a858d7f1cd17b4c8542b01b2bbe4b5c9fa4370e858c3e425169b3651`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:36d03e7613d05ab6ce1c1817bc4d9720beb6999b2ad53544eb5e3a2516cd1ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8958015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad61f6950b1867cb131ac306bfe2a393ccd3dab4507a6325e59c48f2af639b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
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
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0594eef92af6aa29d7428599f3b9e122522e0df39967aea2702a1a7354bc793b`  
		Last Modified: Tue, 12 Nov 2024 02:48:30 GMT  
		Size: 5.9 MB (5861556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed14b98308733affe9fe749214fb8643392c322570578c6ddfbe5251a8ca2db`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b57653849bc6f738b0c3a45512d4f5f55ed7cf0466cd66da9978681b3d05bb`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:424c646570a8c538d99567b966badb8922973ba030077c7d9d5adcbba052386c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d834b5f412a01df4f8c691931cc747d1cbfa65438f1dc948e63e145688149d`

```dockerfile
```

-	Layers:
	-	`sha256:ff72db6a7c559ec37ebb7d4eb71dffcb585101245d8ba8d3bdfbccba6d296c9e`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a7f055eca1521c7f5a89ba5f3dcbff015d57b7a929f8653829c4e6f84164ff2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9855266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75531e0cd58e417f674a8e110cb1b6e032052abc49a34eedf099ba501b1d32b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bd95ee62c7b05e1bf51249d821ab5d9c7323b886d6011744c379d852026d7e`  
		Last Modified: Tue, 12 Nov 2024 03:26:08 GMT  
		Size: 5.8 MB (5766572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20828f336b418c422317d432dc54494c2f6f4697807ed67b33b3bf87374d264`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd330508109963791b4e971f393f42a96ffa843f5e1ece34de92c80dd95e5a9`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:22ac145883a598f4b7c32a900872632569da0619343044db5863844cc5058fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c5b2ebe0e5f3de2734ead969830dbff55bda027a2f6102738f18c7b977ce07`

```dockerfile
```

-	Layers:
	-	`sha256:7cbe0336f7559a824c148c9cb1e5ce3cdf8928a832551a22b11df2774e094d57`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 14.5 KB (14473 bytes)  
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
$ docker pull nats@sha256:cda604f86c6f675320fbd53dce9269d1393938cde088c37491afd1b1a4ddb020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9526654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8bbb69f923453ac9b983b9d3a9d7e88d1f8c9de5b29ecb82922d0fc8bc99da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
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
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a24a04eddab32efb185e6d873c262922dce57394b371a3901e3bb19e5f4cdbc`  
		Last Modified: Tue, 12 Nov 2024 02:57:34 GMT  
		Size: 6.1 MB (6064072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9aa499bc6c83adb2be115e61e0c7a9e080e79501dbc174968339ba9e3bfe4a0`  
		Last Modified: Tue, 12 Nov 2024 02:57:33 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d05fb7412b90c2f9ba0f5842dbb79f53b2bc89fa193ba41fee4a85f0534d04`  
		Last Modified: Tue, 12 Nov 2024 02:57:34 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b5f26e32d54b599383af173aa3afe007e7b2342bad2e9ae78ffac68e49a82d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb3c81387bfd79dbecbffc981bf9b9658f21b3e9606b7880fcedf1261b9d521`

```dockerfile
```

-	Layers:
	-	`sha256:e2b54010f5848cb09c8db6514ef7b759e9ddfd276bc92657148c8b7422c3d2df`  
		Last Modified: Tue, 12 Nov 2024 02:57:33 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-alpine3.20`

```console
$ docker pull nats@sha256:73b0ba5fec5518c5f698597c58d2a3350a2b5ccae43e84c308f8d2da1242deca
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

### `nats:2-alpine3.20` - linux; amd64

```console
$ docker pull nats@sha256:aa536352f09b109b909e8bfbf9859a40601481bb3742ebc7a09cfaf638622407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ede291869d412212887b120efa5c8b7f3b08aefea8f280cd067254c01c2821e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d773e5a5acd4a5185e1795ce442fae0815b4cde8653279c82cb254f75c731910`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 6.2 MB (6205667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae6cea471c207a94e7b03500b522e43c2a3eadd03542e610de9d99ab66afb0`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae68805e7e9a1127a5a8d98e4da64d38cf8b0d9bd426df532b489f42860fd6ea`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:02807cf2f8c136dbf08462f9e4830c0ebe9789135bd35f9dc1b3bed84498f403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7502fcca317f6d32816fbedbe1b62bc47f8c999075143f1668fe57bce064a8`

```dockerfile
```

-	Layers:
	-	`sha256:2d235c7a9ec1b8f79a5b506d4f47baa00cda2f90ab4c8e3e4b95135a10c82667`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.20` - linux; arm variant v6

```console
$ docker pull nats@sha256:08995147ec70b3d9cf6231fcaf9c5693f13f0f8fd2350e601c621f38b84d6e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9237219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d69a74357f1c0cc0b96cfa8306847367e64f3404a70a674e10549211ca3787`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
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
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65afc62adacdff0bf527d9f1b6aaf695b5d37e83fe01a9318f61f316f7f181b6`  
		Last Modified: Tue, 12 Nov 2024 02:43:39 GMT  
		Size: 5.9 MB (5869651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970e0190e0f471373e9e66c70a2752250ed9e69da363c0bfba42143fede6fdf1`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191dbad2f5874fb9d2a78809f1cb2d73967711a343f8a69c0d2feaae390b4b80`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:f9d6d9aa5070fd9051dc1f6b9b181fb2d58de8807e51d6258c1f350ab3b25b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815d234991f683d0c7e6bf47ad52a53158e360aad37d3918ef50be115c7513f7`

```dockerfile
```

-	Layers:
	-	`sha256:4c385d33a858d7f1cd17b4c8542b01b2bbe4b5c9fa4370e858c3e425169b3651`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:36d03e7613d05ab6ce1c1817bc4d9720beb6999b2ad53544eb5e3a2516cd1ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8958015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad61f6950b1867cb131ac306bfe2a393ccd3dab4507a6325e59c48f2af639b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
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
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0594eef92af6aa29d7428599f3b9e122522e0df39967aea2702a1a7354bc793b`  
		Last Modified: Tue, 12 Nov 2024 02:48:30 GMT  
		Size: 5.9 MB (5861556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed14b98308733affe9fe749214fb8643392c322570578c6ddfbe5251a8ca2db`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b57653849bc6f738b0c3a45512d4f5f55ed7cf0466cd66da9978681b3d05bb`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:424c646570a8c538d99567b966badb8922973ba030077c7d9d5adcbba052386c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d834b5f412a01df4f8c691931cc747d1cbfa65438f1dc948e63e145688149d`

```dockerfile
```

-	Layers:
	-	`sha256:ff72db6a7c559ec37ebb7d4eb71dffcb585101245d8ba8d3bdfbccba6d296c9e`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a7f055eca1521c7f5a89ba5f3dcbff015d57b7a929f8653829c4e6f84164ff2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9855266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75531e0cd58e417f674a8e110cb1b6e032052abc49a34eedf099ba501b1d32b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bd95ee62c7b05e1bf51249d821ab5d9c7323b886d6011744c379d852026d7e`  
		Last Modified: Tue, 12 Nov 2024 03:26:08 GMT  
		Size: 5.8 MB (5766572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20828f336b418c422317d432dc54494c2f6f4697807ed67b33b3bf87374d264`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd330508109963791b4e971f393f42a96ffa843f5e1ece34de92c80dd95e5a9`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:22ac145883a598f4b7c32a900872632569da0619343044db5863844cc5058fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c5b2ebe0e5f3de2734ead969830dbff55bda027a2f6102738f18c7b977ce07`

```dockerfile
```

-	Layers:
	-	`sha256:7cbe0336f7559a824c148c9cb1e5ce3cdf8928a832551a22b11df2774e094d57`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 14.5 KB (14473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.20` - linux; ppc64le

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

### `nats:2-alpine3.20` - unknown; unknown

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

### `nats:2-alpine3.20` - linux; s390x

```console
$ docker pull nats@sha256:cda604f86c6f675320fbd53dce9269d1393938cde088c37491afd1b1a4ddb020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9526654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8bbb69f923453ac9b983b9d3a9d7e88d1f8c9de5b29ecb82922d0fc8bc99da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
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
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a24a04eddab32efb185e6d873c262922dce57394b371a3901e3bb19e5f4cdbc`  
		Last Modified: Tue, 12 Nov 2024 02:57:34 GMT  
		Size: 6.1 MB (6064072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9aa499bc6c83adb2be115e61e0c7a9e080e79501dbc174968339ba9e3bfe4a0`  
		Last Modified: Tue, 12 Nov 2024 02:57:33 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d05fb7412b90c2f9ba0f5842dbb79f53b2bc89fa193ba41fee4a85f0534d04`  
		Last Modified: Tue, 12 Nov 2024 02:57:34 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:b5f26e32d54b599383af173aa3afe007e7b2342bad2e9ae78ffac68e49a82d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb3c81387bfd79dbecbffc981bf9b9658f21b3e9606b7880fcedf1261b9d521`

```dockerfile
```

-	Layers:
	-	`sha256:e2b54010f5848cb09c8db6514ef7b759e9ddfd276bc92657148c8b7422c3d2df`  
		Last Modified: Tue, 12 Nov 2024 02:57:33 GMT  
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
$ docker pull nats@sha256:f8924d81bd9732f82846c91bb856438bd2a35819af18351b3adc9e9d037e2198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:053fd6a67430966b5ef4253d8b1cfc23a311da729a9389d83b3dfd01800e63ce
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842d20e36f047cfb078828de10ee4d9abbbd7eebde56d0c84f6d90843adee82a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Tue, 12 Nov 2024 02:02:48 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Nov 2024 02:02:49 GMT
RUN cmd /S /C #(nop) COPY file:6efa011ff84014d148ada9315a3292149a71c3daa1b536499f2b43a2daee2d50 in C:\nats-server.exe 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3c2d0f66b6ae0af6bb08b99b128223baab674d525e452e0991867c2a1173b0`  
		Last Modified: Tue, 12 Nov 2024 02:02:57 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ba4c6aafec94bd41860c1d9e8327b73b0ac64c85b1c317350f3df49318178d`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 5.9 MB (5870082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af1e1e6a4962ecc81604ad1b09ea03a4519d9de02bfd8f36edb94d3f8bef32`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1db4ff41e188b9274e333b99fd768fd30e9023a68547ce0a4f7f910f0e3e88`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c3ee6788b430468c453082a98238ebe894e2beb7699b2dc742b1e842ed0616`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619838cdeb9173ba7f68fc27c3eaf3bbd6cb680b441c766e7f4274f6b25573f6`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:f8924d81bd9732f82846c91bb856438bd2a35819af18351b3adc9e9d037e2198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:053fd6a67430966b5ef4253d8b1cfc23a311da729a9389d83b3dfd01800e63ce
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842d20e36f047cfb078828de10ee4d9abbbd7eebde56d0c84f6d90843adee82a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Tue, 12 Nov 2024 02:02:48 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Nov 2024 02:02:49 GMT
RUN cmd /S /C #(nop) COPY file:6efa011ff84014d148ada9315a3292149a71c3daa1b536499f2b43a2daee2d50 in C:\nats-server.exe 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3c2d0f66b6ae0af6bb08b99b128223baab674d525e452e0991867c2a1173b0`  
		Last Modified: Tue, 12 Nov 2024 02:02:57 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ba4c6aafec94bd41860c1d9e8327b73b0ac64c85b1c317350f3df49318178d`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 5.9 MB (5870082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af1e1e6a4962ecc81604ad1b09ea03a4519d9de02bfd8f36edb94d3f8bef32`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1db4ff41e188b9274e333b99fd768fd30e9023a68547ce0a4f7f910f0e3e88`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c3ee6788b430468c453082a98238ebe894e2beb7699b2dc742b1e842ed0616`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619838cdeb9173ba7f68fc27c3eaf3bbd6cb680b441c766e7f4274f6b25573f6`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1034 bytes)  
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
$ docker pull nats@sha256:a00572f98e370fa7e38673d6f9dbd7491c2980da00b94218476adc4e35fc34b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:a544cd93433d9a20cebec211187257f3dfc5ad64bccfc72019171566d67f7138
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2017374775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0aab012c48e0936fcb2a089535bae300eb2f65bc21e7140d06163652d9b501c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:12:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 14 Nov 2024 20:12:35 GMT
ENV NATS_DOCKERIZED=1
# Thu, 14 Nov 2024 20:12:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 14 Nov 2024 20:12:36 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.22/nats-server-v2.10.22-windows-amd64.zip
# Thu, 14 Nov 2024 20:12:37 GMT
ENV NATS_SERVER_SHASUM=33c8a0c6feb441ec4c7007e0af9ef2a45356d6809cd08ec4871a3d659fc74e91
# Thu, 14 Nov 2024 20:13:06 GMT
RUN Set-PSDebug -Trace 2
# Thu, 14 Nov 2024 20:13:25 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 14 Nov 2024 20:13:25 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Nov 2024 20:13:26 GMT
EXPOSE 4222 6222 8222
# Thu, 14 Nov 2024 20:13:27 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Nov 2024 20:13:28 GMT
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
	-	`sha256:10358d552e245a0f60197403d853dbb7bcd83023506e3226c430831946e9e865`  
		Last Modified: Thu, 14 Nov 2024 20:13:32 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72869b161d8ad342bab228662883909c020f01c6bc4c27871d31fc4f365a046b`  
		Last Modified: Thu, 14 Nov 2024 20:13:32 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a81185dc143775e717174308c22eaf2209b2520f4f0bb1016dbbf92287a7296`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f36bfa3761e70bb198e4579426044ee11dc9c458e328fce82bff4ba248d0f8`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c72cf7ed0a41719c2ce9d90094f3d7e6ae584b33711ff21436ecfef8815d3e21`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4229ea658d6eb6e8f2bfa045b30a1289dd9de99b8b441d6cd9898c3fc49a6aa`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 483.7 KB (483663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81df74489f9de75667f2218291de35e710f354b08ff3334741bce57f8df4d9f4`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 6.2 MB (6224895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25cac8385177c49d1cd2e078613a19421400ed90e9d113e91d66a0c2d1a07ea3`  
		Last Modified: Thu, 14 Nov 2024 20:13:30 GMT  
		Size: 2.0 KB (1960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f25debedaf0706665ea7236d4f8f3f829adde20e8ff97313c36bf2940ef8cff`  
		Last Modified: Thu, 14 Nov 2024 20:13:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5757149326a492b091d121e2dd3671f8a31f56e534f4f9ff33d797a65700053`  
		Last Modified: Thu, 14 Nov 2024 20:13:30 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957afa0f9a92724bcd4c27e34d67fe0a6508ede3c6e9fd1633edafe52e79bfdb`  
		Last Modified: Thu, 14 Nov 2024 20:13:30 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:a00572f98e370fa7e38673d6f9dbd7491c2980da00b94218476adc4e35fc34b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:a544cd93433d9a20cebec211187257f3dfc5ad64bccfc72019171566d67f7138
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2017374775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0aab012c48e0936fcb2a089535bae300eb2f65bc21e7140d06163652d9b501c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:12:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 14 Nov 2024 20:12:35 GMT
ENV NATS_DOCKERIZED=1
# Thu, 14 Nov 2024 20:12:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 14 Nov 2024 20:12:36 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.22/nats-server-v2.10.22-windows-amd64.zip
# Thu, 14 Nov 2024 20:12:37 GMT
ENV NATS_SERVER_SHASUM=33c8a0c6feb441ec4c7007e0af9ef2a45356d6809cd08ec4871a3d659fc74e91
# Thu, 14 Nov 2024 20:13:06 GMT
RUN Set-PSDebug -Trace 2
# Thu, 14 Nov 2024 20:13:25 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 14 Nov 2024 20:13:25 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Nov 2024 20:13:26 GMT
EXPOSE 4222 6222 8222
# Thu, 14 Nov 2024 20:13:27 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Nov 2024 20:13:28 GMT
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
	-	`sha256:10358d552e245a0f60197403d853dbb7bcd83023506e3226c430831946e9e865`  
		Last Modified: Thu, 14 Nov 2024 20:13:32 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72869b161d8ad342bab228662883909c020f01c6bc4c27871d31fc4f365a046b`  
		Last Modified: Thu, 14 Nov 2024 20:13:32 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a81185dc143775e717174308c22eaf2209b2520f4f0bb1016dbbf92287a7296`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f36bfa3761e70bb198e4579426044ee11dc9c458e328fce82bff4ba248d0f8`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c72cf7ed0a41719c2ce9d90094f3d7e6ae584b33711ff21436ecfef8815d3e21`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4229ea658d6eb6e8f2bfa045b30a1289dd9de99b8b441d6cd9898c3fc49a6aa`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 483.7 KB (483663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81df74489f9de75667f2218291de35e710f354b08ff3334741bce57f8df4d9f4`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 6.2 MB (6224895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25cac8385177c49d1cd2e078613a19421400ed90e9d113e91d66a0c2d1a07ea3`  
		Last Modified: Thu, 14 Nov 2024 20:13:30 GMT  
		Size: 2.0 KB (1960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f25debedaf0706665ea7236d4f8f3f829adde20e8ff97313c36bf2940ef8cff`  
		Last Modified: Thu, 14 Nov 2024 20:13:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5757149326a492b091d121e2dd3671f8a31f56e534f4f9ff33d797a65700053`  
		Last Modified: Thu, 14 Nov 2024 20:13:30 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957afa0f9a92724bcd4c27e34d67fe0a6508ede3c6e9fd1633edafe52e79bfdb`  
		Last Modified: Thu, 14 Nov 2024 20:13:30 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:6658c4197669a20542109153a783caccc2642eecd007a491467aeb684d6c1ac0
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
	-	windows version 10.0.17763.6414; amd64

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

### `nats:2.10` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:053fd6a67430966b5ef4253d8b1cfc23a311da729a9389d83b3dfd01800e63ce
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842d20e36f047cfb078828de10ee4d9abbbd7eebde56d0c84f6d90843adee82a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Tue, 12 Nov 2024 02:02:48 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Nov 2024 02:02:49 GMT
RUN cmd /S /C #(nop) COPY file:6efa011ff84014d148ada9315a3292149a71c3daa1b536499f2b43a2daee2d50 in C:\nats-server.exe 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3c2d0f66b6ae0af6bb08b99b128223baab674d525e452e0991867c2a1173b0`  
		Last Modified: Tue, 12 Nov 2024 02:02:57 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ba4c6aafec94bd41860c1d9e8327b73b0ac64c85b1c317350f3df49318178d`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 5.9 MB (5870082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af1e1e6a4962ecc81604ad1b09ea03a4519d9de02bfd8f36edb94d3f8bef32`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1db4ff41e188b9274e333b99fd768fd30e9023a68547ce0a4f7f910f0e3e88`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c3ee6788b430468c453082a98238ebe894e2beb7699b2dc742b1e842ed0616`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619838cdeb9173ba7f68fc27c3eaf3bbd6cb680b441c766e7f4274f6b25573f6`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:73b0ba5fec5518c5f698597c58d2a3350a2b5ccae43e84c308f8d2da1242deca
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
$ docker pull nats@sha256:aa536352f09b109b909e8bfbf9859a40601481bb3742ebc7a09cfaf638622407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ede291869d412212887b120efa5c8b7f3b08aefea8f280cd067254c01c2821e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d773e5a5acd4a5185e1795ce442fae0815b4cde8653279c82cb254f75c731910`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 6.2 MB (6205667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae6cea471c207a94e7b03500b522e43c2a3eadd03542e610de9d99ab66afb0`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae68805e7e9a1127a5a8d98e4da64d38cf8b0d9bd426df532b489f42860fd6ea`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:02807cf2f8c136dbf08462f9e4830c0ebe9789135bd35f9dc1b3bed84498f403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7502fcca317f6d32816fbedbe1b62bc47f8c999075143f1668fe57bce064a8`

```dockerfile
```

-	Layers:
	-	`sha256:2d235c7a9ec1b8f79a5b506d4f47baa00cda2f90ab4c8e3e4b95135a10c82667`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:08995147ec70b3d9cf6231fcaf9c5693f13f0f8fd2350e601c621f38b84d6e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9237219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d69a74357f1c0cc0b96cfa8306847367e64f3404a70a674e10549211ca3787`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
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
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65afc62adacdff0bf527d9f1b6aaf695b5d37e83fe01a9318f61f316f7f181b6`  
		Last Modified: Tue, 12 Nov 2024 02:43:39 GMT  
		Size: 5.9 MB (5869651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970e0190e0f471373e9e66c70a2752250ed9e69da363c0bfba42143fede6fdf1`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191dbad2f5874fb9d2a78809f1cb2d73967711a343f8a69c0d2feaae390b4b80`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f9d6d9aa5070fd9051dc1f6b9b181fb2d58de8807e51d6258c1f350ab3b25b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815d234991f683d0c7e6bf47ad52a53158e360aad37d3918ef50be115c7513f7`

```dockerfile
```

-	Layers:
	-	`sha256:4c385d33a858d7f1cd17b4c8542b01b2bbe4b5c9fa4370e858c3e425169b3651`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:36d03e7613d05ab6ce1c1817bc4d9720beb6999b2ad53544eb5e3a2516cd1ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8958015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad61f6950b1867cb131ac306bfe2a393ccd3dab4507a6325e59c48f2af639b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
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
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0594eef92af6aa29d7428599f3b9e122522e0df39967aea2702a1a7354bc793b`  
		Last Modified: Tue, 12 Nov 2024 02:48:30 GMT  
		Size: 5.9 MB (5861556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed14b98308733affe9fe749214fb8643392c322570578c6ddfbe5251a8ca2db`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b57653849bc6f738b0c3a45512d4f5f55ed7cf0466cd66da9978681b3d05bb`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:424c646570a8c538d99567b966badb8922973ba030077c7d9d5adcbba052386c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d834b5f412a01df4f8c691931cc747d1cbfa65438f1dc948e63e145688149d`

```dockerfile
```

-	Layers:
	-	`sha256:ff72db6a7c559ec37ebb7d4eb71dffcb585101245d8ba8d3bdfbccba6d296c9e`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a7f055eca1521c7f5a89ba5f3dcbff015d57b7a929f8653829c4e6f84164ff2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9855266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75531e0cd58e417f674a8e110cb1b6e032052abc49a34eedf099ba501b1d32b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bd95ee62c7b05e1bf51249d821ab5d9c7323b886d6011744c379d852026d7e`  
		Last Modified: Tue, 12 Nov 2024 03:26:08 GMT  
		Size: 5.8 MB (5766572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20828f336b418c422317d432dc54494c2f6f4697807ed67b33b3bf87374d264`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd330508109963791b4e971f393f42a96ffa843f5e1ece34de92c80dd95e5a9`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:22ac145883a598f4b7c32a900872632569da0619343044db5863844cc5058fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c5b2ebe0e5f3de2734ead969830dbff55bda027a2f6102738f18c7b977ce07`

```dockerfile
```

-	Layers:
	-	`sha256:7cbe0336f7559a824c148c9cb1e5ce3cdf8928a832551a22b11df2774e094d57`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 14.5 KB (14473 bytes)  
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
$ docker pull nats@sha256:cda604f86c6f675320fbd53dce9269d1393938cde088c37491afd1b1a4ddb020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9526654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8bbb69f923453ac9b983b9d3a9d7e88d1f8c9de5b29ecb82922d0fc8bc99da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
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
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a24a04eddab32efb185e6d873c262922dce57394b371a3901e3bb19e5f4cdbc`  
		Last Modified: Tue, 12 Nov 2024 02:57:34 GMT  
		Size: 6.1 MB (6064072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9aa499bc6c83adb2be115e61e0c7a9e080e79501dbc174968339ba9e3bfe4a0`  
		Last Modified: Tue, 12 Nov 2024 02:57:33 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d05fb7412b90c2f9ba0f5842dbb79f53b2bc89fa193ba41fee4a85f0534d04`  
		Last Modified: Tue, 12 Nov 2024 02:57:34 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b5f26e32d54b599383af173aa3afe007e7b2342bad2e9ae78ffac68e49a82d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb3c81387bfd79dbecbffc981bf9b9658f21b3e9606b7880fcedf1261b9d521`

```dockerfile
```

-	Layers:
	-	`sha256:e2b54010f5848cb09c8db6514ef7b759e9ddfd276bc92657148c8b7422c3d2df`  
		Last Modified: Tue, 12 Nov 2024 02:57:33 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-alpine3.20`

```console
$ docker pull nats@sha256:73b0ba5fec5518c5f698597c58d2a3350a2b5ccae43e84c308f8d2da1242deca
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

### `nats:2.10-alpine3.20` - linux; amd64

```console
$ docker pull nats@sha256:aa536352f09b109b909e8bfbf9859a40601481bb3742ebc7a09cfaf638622407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ede291869d412212887b120efa5c8b7f3b08aefea8f280cd067254c01c2821e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d773e5a5acd4a5185e1795ce442fae0815b4cde8653279c82cb254f75c731910`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 6.2 MB (6205667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae6cea471c207a94e7b03500b522e43c2a3eadd03542e610de9d99ab66afb0`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae68805e7e9a1127a5a8d98e4da64d38cf8b0d9bd426df532b489f42860fd6ea`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:02807cf2f8c136dbf08462f9e4830c0ebe9789135bd35f9dc1b3bed84498f403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7502fcca317f6d32816fbedbe1b62bc47f8c999075143f1668fe57bce064a8`

```dockerfile
```

-	Layers:
	-	`sha256:2d235c7a9ec1b8f79a5b506d4f47baa00cda2f90ab4c8e3e4b95135a10c82667`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.20` - linux; arm variant v6

```console
$ docker pull nats@sha256:08995147ec70b3d9cf6231fcaf9c5693f13f0f8fd2350e601c621f38b84d6e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9237219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d69a74357f1c0cc0b96cfa8306847367e64f3404a70a674e10549211ca3787`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
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
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65afc62adacdff0bf527d9f1b6aaf695b5d37e83fe01a9318f61f316f7f181b6`  
		Last Modified: Tue, 12 Nov 2024 02:43:39 GMT  
		Size: 5.9 MB (5869651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970e0190e0f471373e9e66c70a2752250ed9e69da363c0bfba42143fede6fdf1`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191dbad2f5874fb9d2a78809f1cb2d73967711a343f8a69c0d2feaae390b4b80`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:f9d6d9aa5070fd9051dc1f6b9b181fb2d58de8807e51d6258c1f350ab3b25b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815d234991f683d0c7e6bf47ad52a53158e360aad37d3918ef50be115c7513f7`

```dockerfile
```

-	Layers:
	-	`sha256:4c385d33a858d7f1cd17b4c8542b01b2bbe4b5c9fa4370e858c3e425169b3651`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:36d03e7613d05ab6ce1c1817bc4d9720beb6999b2ad53544eb5e3a2516cd1ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8958015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad61f6950b1867cb131ac306bfe2a393ccd3dab4507a6325e59c48f2af639b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
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
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0594eef92af6aa29d7428599f3b9e122522e0df39967aea2702a1a7354bc793b`  
		Last Modified: Tue, 12 Nov 2024 02:48:30 GMT  
		Size: 5.9 MB (5861556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed14b98308733affe9fe749214fb8643392c322570578c6ddfbe5251a8ca2db`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b57653849bc6f738b0c3a45512d4f5f55ed7cf0466cd66da9978681b3d05bb`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:424c646570a8c538d99567b966badb8922973ba030077c7d9d5adcbba052386c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d834b5f412a01df4f8c691931cc747d1cbfa65438f1dc948e63e145688149d`

```dockerfile
```

-	Layers:
	-	`sha256:ff72db6a7c559ec37ebb7d4eb71dffcb585101245d8ba8d3bdfbccba6d296c9e`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a7f055eca1521c7f5a89ba5f3dcbff015d57b7a929f8653829c4e6f84164ff2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9855266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75531e0cd58e417f674a8e110cb1b6e032052abc49a34eedf099ba501b1d32b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bd95ee62c7b05e1bf51249d821ab5d9c7323b886d6011744c379d852026d7e`  
		Last Modified: Tue, 12 Nov 2024 03:26:08 GMT  
		Size: 5.8 MB (5766572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20828f336b418c422317d432dc54494c2f6f4697807ed67b33b3bf87374d264`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd330508109963791b4e971f393f42a96ffa843f5e1ece34de92c80dd95e5a9`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:22ac145883a598f4b7c32a900872632569da0619343044db5863844cc5058fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c5b2ebe0e5f3de2734ead969830dbff55bda027a2f6102738f18c7b977ce07`

```dockerfile
```

-	Layers:
	-	`sha256:7cbe0336f7559a824c148c9cb1e5ce3cdf8928a832551a22b11df2774e094d57`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 14.5 KB (14473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.20` - linux; ppc64le

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

### `nats:2.10-alpine3.20` - unknown; unknown

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

### `nats:2.10-alpine3.20` - linux; s390x

```console
$ docker pull nats@sha256:cda604f86c6f675320fbd53dce9269d1393938cde088c37491afd1b1a4ddb020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9526654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8bbb69f923453ac9b983b9d3a9d7e88d1f8c9de5b29ecb82922d0fc8bc99da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
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
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a24a04eddab32efb185e6d873c262922dce57394b371a3901e3bb19e5f4cdbc`  
		Last Modified: Tue, 12 Nov 2024 02:57:34 GMT  
		Size: 6.1 MB (6064072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9aa499bc6c83adb2be115e61e0c7a9e080e79501dbc174968339ba9e3bfe4a0`  
		Last Modified: Tue, 12 Nov 2024 02:57:33 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d05fb7412b90c2f9ba0f5842dbb79f53b2bc89fa193ba41fee4a85f0534d04`  
		Last Modified: Tue, 12 Nov 2024 02:57:34 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:b5f26e32d54b599383af173aa3afe007e7b2342bad2e9ae78ffac68e49a82d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb3c81387bfd79dbecbffc981bf9b9658f21b3e9606b7880fcedf1261b9d521`

```dockerfile
```

-	Layers:
	-	`sha256:e2b54010f5848cb09c8db6514ef7b759e9ddfd276bc92657148c8b7422c3d2df`  
		Last Modified: Tue, 12 Nov 2024 02:57:33 GMT  
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
$ docker pull nats@sha256:f8924d81bd9732f82846c91bb856438bd2a35819af18351b3adc9e9d037e2198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:2.10-nanoserver` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:053fd6a67430966b5ef4253d8b1cfc23a311da729a9389d83b3dfd01800e63ce
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842d20e36f047cfb078828de10ee4d9abbbd7eebde56d0c84f6d90843adee82a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Tue, 12 Nov 2024 02:02:48 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Nov 2024 02:02:49 GMT
RUN cmd /S /C #(nop) COPY file:6efa011ff84014d148ada9315a3292149a71c3daa1b536499f2b43a2daee2d50 in C:\nats-server.exe 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3c2d0f66b6ae0af6bb08b99b128223baab674d525e452e0991867c2a1173b0`  
		Last Modified: Tue, 12 Nov 2024 02:02:57 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ba4c6aafec94bd41860c1d9e8327b73b0ac64c85b1c317350f3df49318178d`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 5.9 MB (5870082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af1e1e6a4962ecc81604ad1b09ea03a4519d9de02bfd8f36edb94d3f8bef32`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1db4ff41e188b9274e333b99fd768fd30e9023a68547ce0a4f7f910f0e3e88`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c3ee6788b430468c453082a98238ebe894e2beb7699b2dc742b1e842ed0616`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619838cdeb9173ba7f68fc27c3eaf3bbd6cb680b441c766e7f4274f6b25573f6`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-1809`

```console
$ docker pull nats@sha256:f8924d81bd9732f82846c91bb856438bd2a35819af18351b3adc9e9d037e2198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:2.10-nanoserver-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:053fd6a67430966b5ef4253d8b1cfc23a311da729a9389d83b3dfd01800e63ce
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842d20e36f047cfb078828de10ee4d9abbbd7eebde56d0c84f6d90843adee82a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Tue, 12 Nov 2024 02:02:48 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Nov 2024 02:02:49 GMT
RUN cmd /S /C #(nop) COPY file:6efa011ff84014d148ada9315a3292149a71c3daa1b536499f2b43a2daee2d50 in C:\nats-server.exe 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3c2d0f66b6ae0af6bb08b99b128223baab674d525e452e0991867c2a1173b0`  
		Last Modified: Tue, 12 Nov 2024 02:02:57 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ba4c6aafec94bd41860c1d9e8327b73b0ac64c85b1c317350f3df49318178d`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 5.9 MB (5870082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af1e1e6a4962ecc81604ad1b09ea03a4519d9de02bfd8f36edb94d3f8bef32`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1db4ff41e188b9274e333b99fd768fd30e9023a68547ce0a4f7f910f0e3e88`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c3ee6788b430468c453082a98238ebe894e2beb7699b2dc742b1e842ed0616`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619838cdeb9173ba7f68fc27c3eaf3bbd6cb680b441c766e7f4274f6b25573f6`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1034 bytes)  
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
$ docker pull nats@sha256:a00572f98e370fa7e38673d6f9dbd7491c2980da00b94218476adc4e35fc34b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:a544cd93433d9a20cebec211187257f3dfc5ad64bccfc72019171566d67f7138
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2017374775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0aab012c48e0936fcb2a089535bae300eb2f65bc21e7140d06163652d9b501c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:12:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 14 Nov 2024 20:12:35 GMT
ENV NATS_DOCKERIZED=1
# Thu, 14 Nov 2024 20:12:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 14 Nov 2024 20:12:36 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.22/nats-server-v2.10.22-windows-amd64.zip
# Thu, 14 Nov 2024 20:12:37 GMT
ENV NATS_SERVER_SHASUM=33c8a0c6feb441ec4c7007e0af9ef2a45356d6809cd08ec4871a3d659fc74e91
# Thu, 14 Nov 2024 20:13:06 GMT
RUN Set-PSDebug -Trace 2
# Thu, 14 Nov 2024 20:13:25 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 14 Nov 2024 20:13:25 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Nov 2024 20:13:26 GMT
EXPOSE 4222 6222 8222
# Thu, 14 Nov 2024 20:13:27 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Nov 2024 20:13:28 GMT
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
	-	`sha256:10358d552e245a0f60197403d853dbb7bcd83023506e3226c430831946e9e865`  
		Last Modified: Thu, 14 Nov 2024 20:13:32 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72869b161d8ad342bab228662883909c020f01c6bc4c27871d31fc4f365a046b`  
		Last Modified: Thu, 14 Nov 2024 20:13:32 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a81185dc143775e717174308c22eaf2209b2520f4f0bb1016dbbf92287a7296`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f36bfa3761e70bb198e4579426044ee11dc9c458e328fce82bff4ba248d0f8`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c72cf7ed0a41719c2ce9d90094f3d7e6ae584b33711ff21436ecfef8815d3e21`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4229ea658d6eb6e8f2bfa045b30a1289dd9de99b8b441d6cd9898c3fc49a6aa`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 483.7 KB (483663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81df74489f9de75667f2218291de35e710f354b08ff3334741bce57f8df4d9f4`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 6.2 MB (6224895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25cac8385177c49d1cd2e078613a19421400ed90e9d113e91d66a0c2d1a07ea3`  
		Last Modified: Thu, 14 Nov 2024 20:13:30 GMT  
		Size: 2.0 KB (1960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f25debedaf0706665ea7236d4f8f3f829adde20e8ff97313c36bf2940ef8cff`  
		Last Modified: Thu, 14 Nov 2024 20:13:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5757149326a492b091d121e2dd3671f8a31f56e534f4f9ff33d797a65700053`  
		Last Modified: Thu, 14 Nov 2024 20:13:30 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957afa0f9a92724bcd4c27e34d67fe0a6508ede3c6e9fd1633edafe52e79bfdb`  
		Last Modified: Thu, 14 Nov 2024 20:13:30 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-1809`

```console
$ docker pull nats@sha256:a00572f98e370fa7e38673d6f9dbd7491c2980da00b94218476adc4e35fc34b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `nats:2.10-windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:a544cd93433d9a20cebec211187257f3dfc5ad64bccfc72019171566d67f7138
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2017374775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0aab012c48e0936fcb2a089535bae300eb2f65bc21e7140d06163652d9b501c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:12:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 14 Nov 2024 20:12:35 GMT
ENV NATS_DOCKERIZED=1
# Thu, 14 Nov 2024 20:12:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 14 Nov 2024 20:12:36 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.22/nats-server-v2.10.22-windows-amd64.zip
# Thu, 14 Nov 2024 20:12:37 GMT
ENV NATS_SERVER_SHASUM=33c8a0c6feb441ec4c7007e0af9ef2a45356d6809cd08ec4871a3d659fc74e91
# Thu, 14 Nov 2024 20:13:06 GMT
RUN Set-PSDebug -Trace 2
# Thu, 14 Nov 2024 20:13:25 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 14 Nov 2024 20:13:25 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Nov 2024 20:13:26 GMT
EXPOSE 4222 6222 8222
# Thu, 14 Nov 2024 20:13:27 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Nov 2024 20:13:28 GMT
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
	-	`sha256:10358d552e245a0f60197403d853dbb7bcd83023506e3226c430831946e9e865`  
		Last Modified: Thu, 14 Nov 2024 20:13:32 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72869b161d8ad342bab228662883909c020f01c6bc4c27871d31fc4f365a046b`  
		Last Modified: Thu, 14 Nov 2024 20:13:32 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a81185dc143775e717174308c22eaf2209b2520f4f0bb1016dbbf92287a7296`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f36bfa3761e70bb198e4579426044ee11dc9c458e328fce82bff4ba248d0f8`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c72cf7ed0a41719c2ce9d90094f3d7e6ae584b33711ff21436ecfef8815d3e21`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4229ea658d6eb6e8f2bfa045b30a1289dd9de99b8b441d6cd9898c3fc49a6aa`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 483.7 KB (483663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81df74489f9de75667f2218291de35e710f354b08ff3334741bce57f8df4d9f4`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 6.2 MB (6224895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25cac8385177c49d1cd2e078613a19421400ed90e9d113e91d66a0c2d1a07ea3`  
		Last Modified: Thu, 14 Nov 2024 20:13:30 GMT  
		Size: 2.0 KB (1960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f25debedaf0706665ea7236d4f8f3f829adde20e8ff97313c36bf2940ef8cff`  
		Last Modified: Thu, 14 Nov 2024 20:13:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5757149326a492b091d121e2dd3671f8a31f56e534f4f9ff33d797a65700053`  
		Last Modified: Thu, 14 Nov 2024 20:13:30 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957afa0f9a92724bcd4c27e34d67fe0a6508ede3c6e9fd1633edafe52e79bfdb`  
		Last Modified: Thu, 14 Nov 2024 20:13:30 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.22`

```console
$ docker pull nats@sha256:6658c4197669a20542109153a783caccc2642eecd007a491467aeb684d6c1ac0
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
	-	windows version 10.0.17763.6414; amd64

### `nats:2.10.22` - linux; amd64

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

### `nats:2.10.22` - unknown; unknown

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

### `nats:2.10.22` - linux; arm variant v6

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

### `nats:2.10.22` - unknown; unknown

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

### `nats:2.10.22` - linux; arm variant v7

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

### `nats:2.10.22` - unknown; unknown

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

### `nats:2.10.22` - linux; arm64 variant v8

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

### `nats:2.10.22` - unknown; unknown

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

### `nats:2.10.22` - linux; ppc64le

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

### `nats:2.10.22` - unknown; unknown

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

### `nats:2.10.22` - linux; s390x

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

### `nats:2.10.22` - unknown; unknown

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

### `nats:2.10.22` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:053fd6a67430966b5ef4253d8b1cfc23a311da729a9389d83b3dfd01800e63ce
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842d20e36f047cfb078828de10ee4d9abbbd7eebde56d0c84f6d90843adee82a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Tue, 12 Nov 2024 02:02:48 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Nov 2024 02:02:49 GMT
RUN cmd /S /C #(nop) COPY file:6efa011ff84014d148ada9315a3292149a71c3daa1b536499f2b43a2daee2d50 in C:\nats-server.exe 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3c2d0f66b6ae0af6bb08b99b128223baab674d525e452e0991867c2a1173b0`  
		Last Modified: Tue, 12 Nov 2024 02:02:57 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ba4c6aafec94bd41860c1d9e8327b73b0ac64c85b1c317350f3df49318178d`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 5.9 MB (5870082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af1e1e6a4962ecc81604ad1b09ea03a4519d9de02bfd8f36edb94d3f8bef32`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1db4ff41e188b9274e333b99fd768fd30e9023a68547ce0a4f7f910f0e3e88`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c3ee6788b430468c453082a98238ebe894e2beb7699b2dc742b1e842ed0616`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619838cdeb9173ba7f68fc27c3eaf3bbd6cb680b441c766e7f4274f6b25573f6`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.22-alpine`

```console
$ docker pull nats@sha256:73b0ba5fec5518c5f698597c58d2a3350a2b5ccae43e84c308f8d2da1242deca
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

### `nats:2.10.22-alpine` - linux; amd64

```console
$ docker pull nats@sha256:aa536352f09b109b909e8bfbf9859a40601481bb3742ebc7a09cfaf638622407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ede291869d412212887b120efa5c8b7f3b08aefea8f280cd067254c01c2821e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d773e5a5acd4a5185e1795ce442fae0815b4cde8653279c82cb254f75c731910`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 6.2 MB (6205667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae6cea471c207a94e7b03500b522e43c2a3eadd03542e610de9d99ab66afb0`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae68805e7e9a1127a5a8d98e4da64d38cf8b0d9bd426df532b489f42860fd6ea`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.22-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:02807cf2f8c136dbf08462f9e4830c0ebe9789135bd35f9dc1b3bed84498f403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7502fcca317f6d32816fbedbe1b62bc47f8c999075143f1668fe57bce064a8`

```dockerfile
```

-	Layers:
	-	`sha256:2d235c7a9ec1b8f79a5b506d4f47baa00cda2f90ab4c8e3e4b95135a10c82667`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.22-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:08995147ec70b3d9cf6231fcaf9c5693f13f0f8fd2350e601c621f38b84d6e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9237219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d69a74357f1c0cc0b96cfa8306847367e64f3404a70a674e10549211ca3787`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
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
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65afc62adacdff0bf527d9f1b6aaf695b5d37e83fe01a9318f61f316f7f181b6`  
		Last Modified: Tue, 12 Nov 2024 02:43:39 GMT  
		Size: 5.9 MB (5869651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970e0190e0f471373e9e66c70a2752250ed9e69da363c0bfba42143fede6fdf1`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191dbad2f5874fb9d2a78809f1cb2d73967711a343f8a69c0d2feaae390b4b80`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.22-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f9d6d9aa5070fd9051dc1f6b9b181fb2d58de8807e51d6258c1f350ab3b25b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815d234991f683d0c7e6bf47ad52a53158e360aad37d3918ef50be115c7513f7`

```dockerfile
```

-	Layers:
	-	`sha256:4c385d33a858d7f1cd17b4c8542b01b2bbe4b5c9fa4370e858c3e425169b3651`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.22-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:36d03e7613d05ab6ce1c1817bc4d9720beb6999b2ad53544eb5e3a2516cd1ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8958015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad61f6950b1867cb131ac306bfe2a393ccd3dab4507a6325e59c48f2af639b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
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
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0594eef92af6aa29d7428599f3b9e122522e0df39967aea2702a1a7354bc793b`  
		Last Modified: Tue, 12 Nov 2024 02:48:30 GMT  
		Size: 5.9 MB (5861556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed14b98308733affe9fe749214fb8643392c322570578c6ddfbe5251a8ca2db`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b57653849bc6f738b0c3a45512d4f5f55ed7cf0466cd66da9978681b3d05bb`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.22-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:424c646570a8c538d99567b966badb8922973ba030077c7d9d5adcbba052386c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d834b5f412a01df4f8c691931cc747d1cbfa65438f1dc948e63e145688149d`

```dockerfile
```

-	Layers:
	-	`sha256:ff72db6a7c559ec37ebb7d4eb71dffcb585101245d8ba8d3bdfbccba6d296c9e`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.22-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a7f055eca1521c7f5a89ba5f3dcbff015d57b7a929f8653829c4e6f84164ff2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9855266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75531e0cd58e417f674a8e110cb1b6e032052abc49a34eedf099ba501b1d32b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bd95ee62c7b05e1bf51249d821ab5d9c7323b886d6011744c379d852026d7e`  
		Last Modified: Tue, 12 Nov 2024 03:26:08 GMT  
		Size: 5.8 MB (5766572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20828f336b418c422317d432dc54494c2f6f4697807ed67b33b3bf87374d264`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd330508109963791b4e971f393f42a96ffa843f5e1ece34de92c80dd95e5a9`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.22-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:22ac145883a598f4b7c32a900872632569da0619343044db5863844cc5058fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c5b2ebe0e5f3de2734ead969830dbff55bda027a2f6102738f18c7b977ce07`

```dockerfile
```

-	Layers:
	-	`sha256:7cbe0336f7559a824c148c9cb1e5ce3cdf8928a832551a22b11df2774e094d57`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 14.5 KB (14473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.22-alpine` - linux; ppc64le

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

### `nats:2.10.22-alpine` - unknown; unknown

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

### `nats:2.10.22-alpine` - linux; s390x

```console
$ docker pull nats@sha256:cda604f86c6f675320fbd53dce9269d1393938cde088c37491afd1b1a4ddb020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9526654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8bbb69f923453ac9b983b9d3a9d7e88d1f8c9de5b29ecb82922d0fc8bc99da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
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
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a24a04eddab32efb185e6d873c262922dce57394b371a3901e3bb19e5f4cdbc`  
		Last Modified: Tue, 12 Nov 2024 02:57:34 GMT  
		Size: 6.1 MB (6064072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9aa499bc6c83adb2be115e61e0c7a9e080e79501dbc174968339ba9e3bfe4a0`  
		Last Modified: Tue, 12 Nov 2024 02:57:33 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d05fb7412b90c2f9ba0f5842dbb79f53b2bc89fa193ba41fee4a85f0534d04`  
		Last Modified: Tue, 12 Nov 2024 02:57:34 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.22-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b5f26e32d54b599383af173aa3afe007e7b2342bad2e9ae78ffac68e49a82d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb3c81387bfd79dbecbffc981bf9b9658f21b3e9606b7880fcedf1261b9d521`

```dockerfile
```

-	Layers:
	-	`sha256:e2b54010f5848cb09c8db6514ef7b759e9ddfd276bc92657148c8b7422c3d2df`  
		Last Modified: Tue, 12 Nov 2024 02:57:33 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.22-alpine3.20`

```console
$ docker pull nats@sha256:73b0ba5fec5518c5f698597c58d2a3350a2b5ccae43e84c308f8d2da1242deca
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

### `nats:2.10.22-alpine3.20` - linux; amd64

```console
$ docker pull nats@sha256:aa536352f09b109b909e8bfbf9859a40601481bb3742ebc7a09cfaf638622407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ede291869d412212887b120efa5c8b7f3b08aefea8f280cd067254c01c2821e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d773e5a5acd4a5185e1795ce442fae0815b4cde8653279c82cb254f75c731910`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 6.2 MB (6205667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae6cea471c207a94e7b03500b522e43c2a3eadd03542e610de9d99ab66afb0`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae68805e7e9a1127a5a8d98e4da64d38cf8b0d9bd426df532b489f42860fd6ea`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.22-alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:02807cf2f8c136dbf08462f9e4830c0ebe9789135bd35f9dc1b3bed84498f403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7502fcca317f6d32816fbedbe1b62bc47f8c999075143f1668fe57bce064a8`

```dockerfile
```

-	Layers:
	-	`sha256:2d235c7a9ec1b8f79a5b506d4f47baa00cda2f90ab4c8e3e4b95135a10c82667`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.22-alpine3.20` - linux; arm variant v6

```console
$ docker pull nats@sha256:08995147ec70b3d9cf6231fcaf9c5693f13f0f8fd2350e601c621f38b84d6e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9237219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d69a74357f1c0cc0b96cfa8306847367e64f3404a70a674e10549211ca3787`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
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
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65afc62adacdff0bf527d9f1b6aaf695b5d37e83fe01a9318f61f316f7f181b6`  
		Last Modified: Tue, 12 Nov 2024 02:43:39 GMT  
		Size: 5.9 MB (5869651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970e0190e0f471373e9e66c70a2752250ed9e69da363c0bfba42143fede6fdf1`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191dbad2f5874fb9d2a78809f1cb2d73967711a343f8a69c0d2feaae390b4b80`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.22-alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:f9d6d9aa5070fd9051dc1f6b9b181fb2d58de8807e51d6258c1f350ab3b25b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815d234991f683d0c7e6bf47ad52a53158e360aad37d3918ef50be115c7513f7`

```dockerfile
```

-	Layers:
	-	`sha256:4c385d33a858d7f1cd17b4c8542b01b2bbe4b5c9fa4370e858c3e425169b3651`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.22-alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:36d03e7613d05ab6ce1c1817bc4d9720beb6999b2ad53544eb5e3a2516cd1ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8958015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad61f6950b1867cb131ac306bfe2a393ccd3dab4507a6325e59c48f2af639b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
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
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0594eef92af6aa29d7428599f3b9e122522e0df39967aea2702a1a7354bc793b`  
		Last Modified: Tue, 12 Nov 2024 02:48:30 GMT  
		Size: 5.9 MB (5861556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed14b98308733affe9fe749214fb8643392c322570578c6ddfbe5251a8ca2db`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b57653849bc6f738b0c3a45512d4f5f55ed7cf0466cd66da9978681b3d05bb`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.22-alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:424c646570a8c538d99567b966badb8922973ba030077c7d9d5adcbba052386c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d834b5f412a01df4f8c691931cc747d1cbfa65438f1dc948e63e145688149d`

```dockerfile
```

-	Layers:
	-	`sha256:ff72db6a7c559ec37ebb7d4eb71dffcb585101245d8ba8d3bdfbccba6d296c9e`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.22-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a7f055eca1521c7f5a89ba5f3dcbff015d57b7a929f8653829c4e6f84164ff2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9855266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75531e0cd58e417f674a8e110cb1b6e032052abc49a34eedf099ba501b1d32b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bd95ee62c7b05e1bf51249d821ab5d9c7323b886d6011744c379d852026d7e`  
		Last Modified: Tue, 12 Nov 2024 03:26:08 GMT  
		Size: 5.8 MB (5766572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20828f336b418c422317d432dc54494c2f6f4697807ed67b33b3bf87374d264`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd330508109963791b4e971f393f42a96ffa843f5e1ece34de92c80dd95e5a9`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.22-alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:22ac145883a598f4b7c32a900872632569da0619343044db5863844cc5058fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c5b2ebe0e5f3de2734ead969830dbff55bda027a2f6102738f18c7b977ce07`

```dockerfile
```

-	Layers:
	-	`sha256:7cbe0336f7559a824c148c9cb1e5ce3cdf8928a832551a22b11df2774e094d57`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 14.5 KB (14473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.22-alpine3.20` - linux; ppc64le

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

### `nats:2.10.22-alpine3.20` - unknown; unknown

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

### `nats:2.10.22-alpine3.20` - linux; s390x

```console
$ docker pull nats@sha256:cda604f86c6f675320fbd53dce9269d1393938cde088c37491afd1b1a4ddb020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9526654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8bbb69f923453ac9b983b9d3a9d7e88d1f8c9de5b29ecb82922d0fc8bc99da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
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
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a24a04eddab32efb185e6d873c262922dce57394b371a3901e3bb19e5f4cdbc`  
		Last Modified: Tue, 12 Nov 2024 02:57:34 GMT  
		Size: 6.1 MB (6064072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9aa499bc6c83adb2be115e61e0c7a9e080e79501dbc174968339ba9e3bfe4a0`  
		Last Modified: Tue, 12 Nov 2024 02:57:33 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d05fb7412b90c2f9ba0f5842dbb79f53b2bc89fa193ba41fee4a85f0534d04`  
		Last Modified: Tue, 12 Nov 2024 02:57:34 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.22-alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:b5f26e32d54b599383af173aa3afe007e7b2342bad2e9ae78ffac68e49a82d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb3c81387bfd79dbecbffc981bf9b9658f21b3e9606b7880fcedf1261b9d521`

```dockerfile
```

-	Layers:
	-	`sha256:e2b54010f5848cb09c8db6514ef7b759e9ddfd276bc92657148c8b7422c3d2df`  
		Last Modified: Tue, 12 Nov 2024 02:57:33 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.22-linux`

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

### `nats:2.10.22-linux` - linux; amd64

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

### `nats:2.10.22-linux` - unknown; unknown

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

### `nats:2.10.22-linux` - linux; arm variant v6

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

### `nats:2.10.22-linux` - unknown; unknown

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

### `nats:2.10.22-linux` - linux; arm variant v7

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

### `nats:2.10.22-linux` - unknown; unknown

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

### `nats:2.10.22-linux` - linux; arm64 variant v8

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

### `nats:2.10.22-linux` - unknown; unknown

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

### `nats:2.10.22-linux` - linux; ppc64le

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

### `nats:2.10.22-linux` - unknown; unknown

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

### `nats:2.10.22-linux` - linux; s390x

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

### `nats:2.10.22-linux` - unknown; unknown

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

## `nats:2.10.22-nanoserver`

```console
$ docker pull nats@sha256:f8924d81bd9732f82846c91bb856438bd2a35819af18351b3adc9e9d037e2198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:2.10.22-nanoserver` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:053fd6a67430966b5ef4253d8b1cfc23a311da729a9389d83b3dfd01800e63ce
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842d20e36f047cfb078828de10ee4d9abbbd7eebde56d0c84f6d90843adee82a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Tue, 12 Nov 2024 02:02:48 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Nov 2024 02:02:49 GMT
RUN cmd /S /C #(nop) COPY file:6efa011ff84014d148ada9315a3292149a71c3daa1b536499f2b43a2daee2d50 in C:\nats-server.exe 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3c2d0f66b6ae0af6bb08b99b128223baab674d525e452e0991867c2a1173b0`  
		Last Modified: Tue, 12 Nov 2024 02:02:57 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ba4c6aafec94bd41860c1d9e8327b73b0ac64c85b1c317350f3df49318178d`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 5.9 MB (5870082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af1e1e6a4962ecc81604ad1b09ea03a4519d9de02bfd8f36edb94d3f8bef32`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1db4ff41e188b9274e333b99fd768fd30e9023a68547ce0a4f7f910f0e3e88`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c3ee6788b430468c453082a98238ebe894e2beb7699b2dc742b1e842ed0616`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619838cdeb9173ba7f68fc27c3eaf3bbd6cb680b441c766e7f4274f6b25573f6`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.22-nanoserver-1809`

```console
$ docker pull nats@sha256:f8924d81bd9732f82846c91bb856438bd2a35819af18351b3adc9e9d037e2198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:2.10.22-nanoserver-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:053fd6a67430966b5ef4253d8b1cfc23a311da729a9389d83b3dfd01800e63ce
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842d20e36f047cfb078828de10ee4d9abbbd7eebde56d0c84f6d90843adee82a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Tue, 12 Nov 2024 02:02:48 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Nov 2024 02:02:49 GMT
RUN cmd /S /C #(nop) COPY file:6efa011ff84014d148ada9315a3292149a71c3daa1b536499f2b43a2daee2d50 in C:\nats-server.exe 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3c2d0f66b6ae0af6bb08b99b128223baab674d525e452e0991867c2a1173b0`  
		Last Modified: Tue, 12 Nov 2024 02:02:57 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ba4c6aafec94bd41860c1d9e8327b73b0ac64c85b1c317350f3df49318178d`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 5.9 MB (5870082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af1e1e6a4962ecc81604ad1b09ea03a4519d9de02bfd8f36edb94d3f8bef32`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1db4ff41e188b9274e333b99fd768fd30e9023a68547ce0a4f7f910f0e3e88`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c3ee6788b430468c453082a98238ebe894e2beb7699b2dc742b1e842ed0616`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619838cdeb9173ba7f68fc27c3eaf3bbd6cb680b441c766e7f4274f6b25573f6`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.22-scratch`

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

### `nats:2.10.22-scratch` - linux; amd64

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

### `nats:2.10.22-scratch` - unknown; unknown

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

### `nats:2.10.22-scratch` - linux; arm variant v6

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

### `nats:2.10.22-scratch` - unknown; unknown

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

### `nats:2.10.22-scratch` - linux; arm variant v7

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

### `nats:2.10.22-scratch` - unknown; unknown

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

### `nats:2.10.22-scratch` - linux; arm64 variant v8

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

### `nats:2.10.22-scratch` - unknown; unknown

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

### `nats:2.10.22-scratch` - linux; ppc64le

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

### `nats:2.10.22-scratch` - unknown; unknown

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

### `nats:2.10.22-scratch` - linux; s390x

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

### `nats:2.10.22-scratch` - unknown; unknown

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

## `nats:2.10.22-windowsservercore`

```console
$ docker pull nats@sha256:a00572f98e370fa7e38673d6f9dbd7491c2980da00b94218476adc4e35fc34b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `nats:2.10.22-windowsservercore` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:a544cd93433d9a20cebec211187257f3dfc5ad64bccfc72019171566d67f7138
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2017374775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0aab012c48e0936fcb2a089535bae300eb2f65bc21e7140d06163652d9b501c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:12:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 14 Nov 2024 20:12:35 GMT
ENV NATS_DOCKERIZED=1
# Thu, 14 Nov 2024 20:12:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 14 Nov 2024 20:12:36 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.22/nats-server-v2.10.22-windows-amd64.zip
# Thu, 14 Nov 2024 20:12:37 GMT
ENV NATS_SERVER_SHASUM=33c8a0c6feb441ec4c7007e0af9ef2a45356d6809cd08ec4871a3d659fc74e91
# Thu, 14 Nov 2024 20:13:06 GMT
RUN Set-PSDebug -Trace 2
# Thu, 14 Nov 2024 20:13:25 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 14 Nov 2024 20:13:25 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Nov 2024 20:13:26 GMT
EXPOSE 4222 6222 8222
# Thu, 14 Nov 2024 20:13:27 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Nov 2024 20:13:28 GMT
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
	-	`sha256:10358d552e245a0f60197403d853dbb7bcd83023506e3226c430831946e9e865`  
		Last Modified: Thu, 14 Nov 2024 20:13:32 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72869b161d8ad342bab228662883909c020f01c6bc4c27871d31fc4f365a046b`  
		Last Modified: Thu, 14 Nov 2024 20:13:32 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a81185dc143775e717174308c22eaf2209b2520f4f0bb1016dbbf92287a7296`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f36bfa3761e70bb198e4579426044ee11dc9c458e328fce82bff4ba248d0f8`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c72cf7ed0a41719c2ce9d90094f3d7e6ae584b33711ff21436ecfef8815d3e21`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4229ea658d6eb6e8f2bfa045b30a1289dd9de99b8b441d6cd9898c3fc49a6aa`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 483.7 KB (483663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81df74489f9de75667f2218291de35e710f354b08ff3334741bce57f8df4d9f4`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 6.2 MB (6224895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25cac8385177c49d1cd2e078613a19421400ed90e9d113e91d66a0c2d1a07ea3`  
		Last Modified: Thu, 14 Nov 2024 20:13:30 GMT  
		Size: 2.0 KB (1960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f25debedaf0706665ea7236d4f8f3f829adde20e8ff97313c36bf2940ef8cff`  
		Last Modified: Thu, 14 Nov 2024 20:13:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5757149326a492b091d121e2dd3671f8a31f56e534f4f9ff33d797a65700053`  
		Last Modified: Thu, 14 Nov 2024 20:13:30 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957afa0f9a92724bcd4c27e34d67fe0a6508ede3c6e9fd1633edafe52e79bfdb`  
		Last Modified: Thu, 14 Nov 2024 20:13:30 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.22-windowsservercore-1809`

```console
$ docker pull nats@sha256:a00572f98e370fa7e38673d6f9dbd7491c2980da00b94218476adc4e35fc34b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `nats:2.10.22-windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:a544cd93433d9a20cebec211187257f3dfc5ad64bccfc72019171566d67f7138
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2017374775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0aab012c48e0936fcb2a089535bae300eb2f65bc21e7140d06163652d9b501c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:12:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 14 Nov 2024 20:12:35 GMT
ENV NATS_DOCKERIZED=1
# Thu, 14 Nov 2024 20:12:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 14 Nov 2024 20:12:36 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.22/nats-server-v2.10.22-windows-amd64.zip
# Thu, 14 Nov 2024 20:12:37 GMT
ENV NATS_SERVER_SHASUM=33c8a0c6feb441ec4c7007e0af9ef2a45356d6809cd08ec4871a3d659fc74e91
# Thu, 14 Nov 2024 20:13:06 GMT
RUN Set-PSDebug -Trace 2
# Thu, 14 Nov 2024 20:13:25 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 14 Nov 2024 20:13:25 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Nov 2024 20:13:26 GMT
EXPOSE 4222 6222 8222
# Thu, 14 Nov 2024 20:13:27 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Nov 2024 20:13:28 GMT
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
	-	`sha256:10358d552e245a0f60197403d853dbb7bcd83023506e3226c430831946e9e865`  
		Last Modified: Thu, 14 Nov 2024 20:13:32 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72869b161d8ad342bab228662883909c020f01c6bc4c27871d31fc4f365a046b`  
		Last Modified: Thu, 14 Nov 2024 20:13:32 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a81185dc143775e717174308c22eaf2209b2520f4f0bb1016dbbf92287a7296`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f36bfa3761e70bb198e4579426044ee11dc9c458e328fce82bff4ba248d0f8`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c72cf7ed0a41719c2ce9d90094f3d7e6ae584b33711ff21436ecfef8815d3e21`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4229ea658d6eb6e8f2bfa045b30a1289dd9de99b8b441d6cd9898c3fc49a6aa`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 483.7 KB (483663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81df74489f9de75667f2218291de35e710f354b08ff3334741bce57f8df4d9f4`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 6.2 MB (6224895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25cac8385177c49d1cd2e078613a19421400ed90e9d113e91d66a0c2d1a07ea3`  
		Last Modified: Thu, 14 Nov 2024 20:13:30 GMT  
		Size: 2.0 KB (1960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f25debedaf0706665ea7236d4f8f3f829adde20e8ff97313c36bf2940ef8cff`  
		Last Modified: Thu, 14 Nov 2024 20:13:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5757149326a492b091d121e2dd3671f8a31f56e534f4f9ff33d797a65700053`  
		Last Modified: Thu, 14 Nov 2024 20:13:30 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957afa0f9a92724bcd4c27e34d67fe0a6508ede3c6e9fd1633edafe52e79bfdb`  
		Last Modified: Thu, 14 Nov 2024 20:13:30 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:73b0ba5fec5518c5f698597c58d2a3350a2b5ccae43e84c308f8d2da1242deca
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
$ docker pull nats@sha256:aa536352f09b109b909e8bfbf9859a40601481bb3742ebc7a09cfaf638622407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ede291869d412212887b120efa5c8b7f3b08aefea8f280cd067254c01c2821e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d773e5a5acd4a5185e1795ce442fae0815b4cde8653279c82cb254f75c731910`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 6.2 MB (6205667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae6cea471c207a94e7b03500b522e43c2a3eadd03542e610de9d99ab66afb0`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae68805e7e9a1127a5a8d98e4da64d38cf8b0d9bd426df532b489f42860fd6ea`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:02807cf2f8c136dbf08462f9e4830c0ebe9789135bd35f9dc1b3bed84498f403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7502fcca317f6d32816fbedbe1b62bc47f8c999075143f1668fe57bce064a8`

```dockerfile
```

-	Layers:
	-	`sha256:2d235c7a9ec1b8f79a5b506d4f47baa00cda2f90ab4c8e3e4b95135a10c82667`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:08995147ec70b3d9cf6231fcaf9c5693f13f0f8fd2350e601c621f38b84d6e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9237219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d69a74357f1c0cc0b96cfa8306847367e64f3404a70a674e10549211ca3787`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
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
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65afc62adacdff0bf527d9f1b6aaf695b5d37e83fe01a9318f61f316f7f181b6`  
		Last Modified: Tue, 12 Nov 2024 02:43:39 GMT  
		Size: 5.9 MB (5869651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970e0190e0f471373e9e66c70a2752250ed9e69da363c0bfba42143fede6fdf1`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191dbad2f5874fb9d2a78809f1cb2d73967711a343f8a69c0d2feaae390b4b80`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f9d6d9aa5070fd9051dc1f6b9b181fb2d58de8807e51d6258c1f350ab3b25b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815d234991f683d0c7e6bf47ad52a53158e360aad37d3918ef50be115c7513f7`

```dockerfile
```

-	Layers:
	-	`sha256:4c385d33a858d7f1cd17b4c8542b01b2bbe4b5c9fa4370e858c3e425169b3651`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:36d03e7613d05ab6ce1c1817bc4d9720beb6999b2ad53544eb5e3a2516cd1ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8958015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad61f6950b1867cb131ac306bfe2a393ccd3dab4507a6325e59c48f2af639b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
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
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0594eef92af6aa29d7428599f3b9e122522e0df39967aea2702a1a7354bc793b`  
		Last Modified: Tue, 12 Nov 2024 02:48:30 GMT  
		Size: 5.9 MB (5861556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed14b98308733affe9fe749214fb8643392c322570578c6ddfbe5251a8ca2db`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b57653849bc6f738b0c3a45512d4f5f55ed7cf0466cd66da9978681b3d05bb`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:424c646570a8c538d99567b966badb8922973ba030077c7d9d5adcbba052386c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d834b5f412a01df4f8c691931cc747d1cbfa65438f1dc948e63e145688149d`

```dockerfile
```

-	Layers:
	-	`sha256:ff72db6a7c559ec37ebb7d4eb71dffcb585101245d8ba8d3bdfbccba6d296c9e`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a7f055eca1521c7f5a89ba5f3dcbff015d57b7a929f8653829c4e6f84164ff2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9855266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75531e0cd58e417f674a8e110cb1b6e032052abc49a34eedf099ba501b1d32b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bd95ee62c7b05e1bf51249d821ab5d9c7323b886d6011744c379d852026d7e`  
		Last Modified: Tue, 12 Nov 2024 03:26:08 GMT  
		Size: 5.8 MB (5766572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20828f336b418c422317d432dc54494c2f6f4697807ed67b33b3bf87374d264`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd330508109963791b4e971f393f42a96ffa843f5e1ece34de92c80dd95e5a9`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:22ac145883a598f4b7c32a900872632569da0619343044db5863844cc5058fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c5b2ebe0e5f3de2734ead969830dbff55bda027a2f6102738f18c7b977ce07`

```dockerfile
```

-	Layers:
	-	`sha256:7cbe0336f7559a824c148c9cb1e5ce3cdf8928a832551a22b11df2774e094d57`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 14.5 KB (14473 bytes)  
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
$ docker pull nats@sha256:cda604f86c6f675320fbd53dce9269d1393938cde088c37491afd1b1a4ddb020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9526654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8bbb69f923453ac9b983b9d3a9d7e88d1f8c9de5b29ecb82922d0fc8bc99da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
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
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a24a04eddab32efb185e6d873c262922dce57394b371a3901e3bb19e5f4cdbc`  
		Last Modified: Tue, 12 Nov 2024 02:57:34 GMT  
		Size: 6.1 MB (6064072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9aa499bc6c83adb2be115e61e0c7a9e080e79501dbc174968339ba9e3bfe4a0`  
		Last Modified: Tue, 12 Nov 2024 02:57:33 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d05fb7412b90c2f9ba0f5842dbb79f53b2bc89fa193ba41fee4a85f0534d04`  
		Last Modified: Tue, 12 Nov 2024 02:57:34 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b5f26e32d54b599383af173aa3afe007e7b2342bad2e9ae78ffac68e49a82d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb3c81387bfd79dbecbffc981bf9b9658f21b3e9606b7880fcedf1261b9d521`

```dockerfile
```

-	Layers:
	-	`sha256:e2b54010f5848cb09c8db6514ef7b759e9ddfd276bc92657148c8b7422c3d2df`  
		Last Modified: Tue, 12 Nov 2024 02:57:33 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:alpine3.20`

```console
$ docker pull nats@sha256:73b0ba5fec5518c5f698597c58d2a3350a2b5ccae43e84c308f8d2da1242deca
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

### `nats:alpine3.20` - linux; amd64

```console
$ docker pull nats@sha256:aa536352f09b109b909e8bfbf9859a40601481bb3742ebc7a09cfaf638622407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ede291869d412212887b120efa5c8b7f3b08aefea8f280cd067254c01c2821e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d773e5a5acd4a5185e1795ce442fae0815b4cde8653279c82cb254f75c731910`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 6.2 MB (6205667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae6cea471c207a94e7b03500b522e43c2a3eadd03542e610de9d99ab66afb0`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae68805e7e9a1127a5a8d98e4da64d38cf8b0d9bd426df532b489f42860fd6ea`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:02807cf2f8c136dbf08462f9e4830c0ebe9789135bd35f9dc1b3bed84498f403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7502fcca317f6d32816fbedbe1b62bc47f8c999075143f1668fe57bce064a8`

```dockerfile
```

-	Layers:
	-	`sha256:2d235c7a9ec1b8f79a5b506d4f47baa00cda2f90ab4c8e3e4b95135a10c82667`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.20` - linux; arm variant v6

```console
$ docker pull nats@sha256:08995147ec70b3d9cf6231fcaf9c5693f13f0f8fd2350e601c621f38b84d6e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9237219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d69a74357f1c0cc0b96cfa8306847367e64f3404a70a674e10549211ca3787`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
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
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65afc62adacdff0bf527d9f1b6aaf695b5d37e83fe01a9318f61f316f7f181b6`  
		Last Modified: Tue, 12 Nov 2024 02:43:39 GMT  
		Size: 5.9 MB (5869651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970e0190e0f471373e9e66c70a2752250ed9e69da363c0bfba42143fede6fdf1`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191dbad2f5874fb9d2a78809f1cb2d73967711a343f8a69c0d2feaae390b4b80`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:f9d6d9aa5070fd9051dc1f6b9b181fb2d58de8807e51d6258c1f350ab3b25b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815d234991f683d0c7e6bf47ad52a53158e360aad37d3918ef50be115c7513f7`

```dockerfile
```

-	Layers:
	-	`sha256:4c385d33a858d7f1cd17b4c8542b01b2bbe4b5c9fa4370e858c3e425169b3651`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:36d03e7613d05ab6ce1c1817bc4d9720beb6999b2ad53544eb5e3a2516cd1ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8958015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad61f6950b1867cb131ac306bfe2a393ccd3dab4507a6325e59c48f2af639b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
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
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0594eef92af6aa29d7428599f3b9e122522e0df39967aea2702a1a7354bc793b`  
		Last Modified: Tue, 12 Nov 2024 02:48:30 GMT  
		Size: 5.9 MB (5861556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed14b98308733affe9fe749214fb8643392c322570578c6ddfbe5251a8ca2db`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b57653849bc6f738b0c3a45512d4f5f55ed7cf0466cd66da9978681b3d05bb`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:424c646570a8c538d99567b966badb8922973ba030077c7d9d5adcbba052386c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d834b5f412a01df4f8c691931cc747d1cbfa65438f1dc948e63e145688149d`

```dockerfile
```

-	Layers:
	-	`sha256:ff72db6a7c559ec37ebb7d4eb71dffcb585101245d8ba8d3bdfbccba6d296c9e`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a7f055eca1521c7f5a89ba5f3dcbff015d57b7a929f8653829c4e6f84164ff2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9855266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75531e0cd58e417f674a8e110cb1b6e032052abc49a34eedf099ba501b1d32b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bd95ee62c7b05e1bf51249d821ab5d9c7323b886d6011744c379d852026d7e`  
		Last Modified: Tue, 12 Nov 2024 03:26:08 GMT  
		Size: 5.8 MB (5766572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20828f336b418c422317d432dc54494c2f6f4697807ed67b33b3bf87374d264`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd330508109963791b4e971f393f42a96ffa843f5e1ece34de92c80dd95e5a9`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:22ac145883a598f4b7c32a900872632569da0619343044db5863844cc5058fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c5b2ebe0e5f3de2734ead969830dbff55bda027a2f6102738f18c7b977ce07`

```dockerfile
```

-	Layers:
	-	`sha256:7cbe0336f7559a824c148c9cb1e5ce3cdf8928a832551a22b11df2774e094d57`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 14.5 KB (14473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.20` - linux; ppc64le

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

### `nats:alpine3.20` - unknown; unknown

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

### `nats:alpine3.20` - linux; s390x

```console
$ docker pull nats@sha256:cda604f86c6f675320fbd53dce9269d1393938cde088c37491afd1b1a4ddb020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9526654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8bbb69f923453ac9b983b9d3a9d7e88d1f8c9de5b29ecb82922d0fc8bc99da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
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
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a24a04eddab32efb185e6d873c262922dce57394b371a3901e3bb19e5f4cdbc`  
		Last Modified: Tue, 12 Nov 2024 02:57:34 GMT  
		Size: 6.1 MB (6064072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9aa499bc6c83adb2be115e61e0c7a9e080e79501dbc174968339ba9e3bfe4a0`  
		Last Modified: Tue, 12 Nov 2024 02:57:33 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d05fb7412b90c2f9ba0f5842dbb79f53b2bc89fa193ba41fee4a85f0534d04`  
		Last Modified: Tue, 12 Nov 2024 02:57:34 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:b5f26e32d54b599383af173aa3afe007e7b2342bad2e9ae78ffac68e49a82d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb3c81387bfd79dbecbffc981bf9b9658f21b3e9606b7880fcedf1261b9d521`

```dockerfile
```

-	Layers:
	-	`sha256:e2b54010f5848cb09c8db6514ef7b759e9ddfd276bc92657148c8b7422c3d2df`  
		Last Modified: Tue, 12 Nov 2024 02:57:33 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:latest`

```console
$ docker pull nats@sha256:6658c4197669a20542109153a783caccc2642eecd007a491467aeb684d6c1ac0
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
	-	windows version 10.0.17763.6414; amd64

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

### `nats:latest` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:053fd6a67430966b5ef4253d8b1cfc23a311da729a9389d83b3dfd01800e63ce
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842d20e36f047cfb078828de10ee4d9abbbd7eebde56d0c84f6d90843adee82a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Tue, 12 Nov 2024 02:02:48 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Nov 2024 02:02:49 GMT
RUN cmd /S /C #(nop) COPY file:6efa011ff84014d148ada9315a3292149a71c3daa1b536499f2b43a2daee2d50 in C:\nats-server.exe 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3c2d0f66b6ae0af6bb08b99b128223baab674d525e452e0991867c2a1173b0`  
		Last Modified: Tue, 12 Nov 2024 02:02:57 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ba4c6aafec94bd41860c1d9e8327b73b0ac64c85b1c317350f3df49318178d`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 5.9 MB (5870082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af1e1e6a4962ecc81604ad1b09ea03a4519d9de02bfd8f36edb94d3f8bef32`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1db4ff41e188b9274e333b99fd768fd30e9023a68547ce0a4f7f910f0e3e88`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c3ee6788b430468c453082a98238ebe894e2beb7699b2dc742b1e842ed0616`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619838cdeb9173ba7f68fc27c3eaf3bbd6cb680b441c766e7f4274f6b25573f6`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1034 bytes)  
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
$ docker pull nats@sha256:f8924d81bd9732f82846c91bb856438bd2a35819af18351b3adc9e9d037e2198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:nanoserver` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:053fd6a67430966b5ef4253d8b1cfc23a311da729a9389d83b3dfd01800e63ce
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842d20e36f047cfb078828de10ee4d9abbbd7eebde56d0c84f6d90843adee82a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Tue, 12 Nov 2024 02:02:48 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Nov 2024 02:02:49 GMT
RUN cmd /S /C #(nop) COPY file:6efa011ff84014d148ada9315a3292149a71c3daa1b536499f2b43a2daee2d50 in C:\nats-server.exe 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3c2d0f66b6ae0af6bb08b99b128223baab674d525e452e0991867c2a1173b0`  
		Last Modified: Tue, 12 Nov 2024 02:02:57 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ba4c6aafec94bd41860c1d9e8327b73b0ac64c85b1c317350f3df49318178d`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 5.9 MB (5870082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af1e1e6a4962ecc81604ad1b09ea03a4519d9de02bfd8f36edb94d3f8bef32`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1db4ff41e188b9274e333b99fd768fd30e9023a68547ce0a4f7f910f0e3e88`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c3ee6788b430468c453082a98238ebe894e2beb7699b2dc742b1e842ed0616`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619838cdeb9173ba7f68fc27c3eaf3bbd6cb680b441c766e7f4274f6b25573f6`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:f8924d81bd9732f82846c91bb856438bd2a35819af18351b3adc9e9d037e2198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:053fd6a67430966b5ef4253d8b1cfc23a311da729a9389d83b3dfd01800e63ce
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842d20e36f047cfb078828de10ee4d9abbbd7eebde56d0c84f6d90843adee82a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Tue, 12 Nov 2024 02:02:48 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Nov 2024 02:02:49 GMT
RUN cmd /S /C #(nop) COPY file:6efa011ff84014d148ada9315a3292149a71c3daa1b536499f2b43a2daee2d50 in C:\nats-server.exe 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3c2d0f66b6ae0af6bb08b99b128223baab674d525e452e0991867c2a1173b0`  
		Last Modified: Tue, 12 Nov 2024 02:02:57 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ba4c6aafec94bd41860c1d9e8327b73b0ac64c85b1c317350f3df49318178d`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 5.9 MB (5870082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af1e1e6a4962ecc81604ad1b09ea03a4519d9de02bfd8f36edb94d3f8bef32`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1db4ff41e188b9274e333b99fd768fd30e9023a68547ce0a4f7f910f0e3e88`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c3ee6788b430468c453082a98238ebe894e2beb7699b2dc742b1e842ed0616`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619838cdeb9173ba7f68fc27c3eaf3bbd6cb680b441c766e7f4274f6b25573f6`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1034 bytes)  
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
$ docker pull nats@sha256:a00572f98e370fa7e38673d6f9dbd7491c2980da00b94218476adc4e35fc34b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `nats:windowsservercore` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:a544cd93433d9a20cebec211187257f3dfc5ad64bccfc72019171566d67f7138
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2017374775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0aab012c48e0936fcb2a089535bae300eb2f65bc21e7140d06163652d9b501c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:12:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 14 Nov 2024 20:12:35 GMT
ENV NATS_DOCKERIZED=1
# Thu, 14 Nov 2024 20:12:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 14 Nov 2024 20:12:36 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.22/nats-server-v2.10.22-windows-amd64.zip
# Thu, 14 Nov 2024 20:12:37 GMT
ENV NATS_SERVER_SHASUM=33c8a0c6feb441ec4c7007e0af9ef2a45356d6809cd08ec4871a3d659fc74e91
# Thu, 14 Nov 2024 20:13:06 GMT
RUN Set-PSDebug -Trace 2
# Thu, 14 Nov 2024 20:13:25 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 14 Nov 2024 20:13:25 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Nov 2024 20:13:26 GMT
EXPOSE 4222 6222 8222
# Thu, 14 Nov 2024 20:13:27 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Nov 2024 20:13:28 GMT
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
	-	`sha256:10358d552e245a0f60197403d853dbb7bcd83023506e3226c430831946e9e865`  
		Last Modified: Thu, 14 Nov 2024 20:13:32 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72869b161d8ad342bab228662883909c020f01c6bc4c27871d31fc4f365a046b`  
		Last Modified: Thu, 14 Nov 2024 20:13:32 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a81185dc143775e717174308c22eaf2209b2520f4f0bb1016dbbf92287a7296`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f36bfa3761e70bb198e4579426044ee11dc9c458e328fce82bff4ba248d0f8`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c72cf7ed0a41719c2ce9d90094f3d7e6ae584b33711ff21436ecfef8815d3e21`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4229ea658d6eb6e8f2bfa045b30a1289dd9de99b8b441d6cd9898c3fc49a6aa`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 483.7 KB (483663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81df74489f9de75667f2218291de35e710f354b08ff3334741bce57f8df4d9f4`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 6.2 MB (6224895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25cac8385177c49d1cd2e078613a19421400ed90e9d113e91d66a0c2d1a07ea3`  
		Last Modified: Thu, 14 Nov 2024 20:13:30 GMT  
		Size: 2.0 KB (1960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f25debedaf0706665ea7236d4f8f3f829adde20e8ff97313c36bf2940ef8cff`  
		Last Modified: Thu, 14 Nov 2024 20:13:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5757149326a492b091d121e2dd3671f8a31f56e534f4f9ff33d797a65700053`  
		Last Modified: Thu, 14 Nov 2024 20:13:30 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957afa0f9a92724bcd4c27e34d67fe0a6508ede3c6e9fd1633edafe52e79bfdb`  
		Last Modified: Thu, 14 Nov 2024 20:13:30 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:a00572f98e370fa7e38673d6f9dbd7491c2980da00b94218476adc4e35fc34b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:a544cd93433d9a20cebec211187257f3dfc5ad64bccfc72019171566d67f7138
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2017374775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0aab012c48e0936fcb2a089535bae300eb2f65bc21e7140d06163652d9b501c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:12:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 14 Nov 2024 20:12:35 GMT
ENV NATS_DOCKERIZED=1
# Thu, 14 Nov 2024 20:12:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 14 Nov 2024 20:12:36 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.22/nats-server-v2.10.22-windows-amd64.zip
# Thu, 14 Nov 2024 20:12:37 GMT
ENV NATS_SERVER_SHASUM=33c8a0c6feb441ec4c7007e0af9ef2a45356d6809cd08ec4871a3d659fc74e91
# Thu, 14 Nov 2024 20:13:06 GMT
RUN Set-PSDebug -Trace 2
# Thu, 14 Nov 2024 20:13:25 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 14 Nov 2024 20:13:25 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Nov 2024 20:13:26 GMT
EXPOSE 4222 6222 8222
# Thu, 14 Nov 2024 20:13:27 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Nov 2024 20:13:28 GMT
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
	-	`sha256:10358d552e245a0f60197403d853dbb7bcd83023506e3226c430831946e9e865`  
		Last Modified: Thu, 14 Nov 2024 20:13:32 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72869b161d8ad342bab228662883909c020f01c6bc4c27871d31fc4f365a046b`  
		Last Modified: Thu, 14 Nov 2024 20:13:32 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a81185dc143775e717174308c22eaf2209b2520f4f0bb1016dbbf92287a7296`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f36bfa3761e70bb198e4579426044ee11dc9c458e328fce82bff4ba248d0f8`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c72cf7ed0a41719c2ce9d90094f3d7e6ae584b33711ff21436ecfef8815d3e21`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4229ea658d6eb6e8f2bfa045b30a1289dd9de99b8b441d6cd9898c3fc49a6aa`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 483.7 KB (483663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81df74489f9de75667f2218291de35e710f354b08ff3334741bce57f8df4d9f4`  
		Last Modified: Thu, 14 Nov 2024 20:13:31 GMT  
		Size: 6.2 MB (6224895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25cac8385177c49d1cd2e078613a19421400ed90e9d113e91d66a0c2d1a07ea3`  
		Last Modified: Thu, 14 Nov 2024 20:13:30 GMT  
		Size: 2.0 KB (1960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f25debedaf0706665ea7236d4f8f3f829adde20e8ff97313c36bf2940ef8cff`  
		Last Modified: Thu, 14 Nov 2024 20:13:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5757149326a492b091d121e2dd3671f8a31f56e534f4f9ff33d797a65700053`  
		Last Modified: Thu, 14 Nov 2024 20:13:30 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957afa0f9a92724bcd4c27e34d67fe0a6508ede3c6e9fd1633edafe52e79bfdb`  
		Last Modified: Thu, 14 Nov 2024 20:13:30 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
