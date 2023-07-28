## `debian:stable-backports`

```console
$ docker pull debian@sha256:84f59924918184ee55b34f5a5d1253a0b0c77e486b683f289b14e3440c1aff3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:c05ba525395fad083646abb88998f557a1f3be0775aff3972cec3b55004234fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49557591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:330d248e40fe0181c506883c8707b28a918b04221b7d7a4c454c48dcecef80f7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:26:44 GMT
ADD file:467d54fcdcc4a4fc484eb81623a50891c72242f1da2748a7616413dc449fad22 in / 
# Thu, 27 Jul 2023 23:26:44 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:26:48 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1924af148565f8d4a8be4dab08aa865788130cd4461a64b42f5470404fb3f613`  
		Last Modified: Thu, 27 Jul 2023 23:32:41 GMT  
		Size: 49.6 MB (49557366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073b60c96f531b6e2cdfad88bacd7360d600a49d9b19fcd108b0e173b3b3c2be`  
		Last Modified: Thu, 27 Jul 2023 23:32:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:ab5b6494c0fa5554e9a57f9961802bde658934cbee71cc57a3d8047590ddb1c6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47415123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fcf4a159b2c4e426ef1c0d981dc0d5b61e96262c7756db5987a1d63bc6d79d8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:49:22 GMT
ADD file:8f568232a57d693c9607a4bfb4953e58e90ddf6a40fd78ebb1fd6e6d41ef24c6 in / 
# Thu, 27 Jul 2023 23:49:23 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:49:26 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9688d95a3b850e726b035b41a8770f830ce4b26f8b903aff1450c1aa87c9bb6f`  
		Last Modified: Thu, 27 Jul 2023 23:53:34 GMT  
		Size: 47.4 MB (47414900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04ddd9d555e086c277f947bdc0118f659811cae264cafca8066232774ada3ca`  
		Last Modified: Thu, 27 Jul 2023 23:53:43 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:7fa92daf530a3c223bc3052052a7e2e37589eb96c79560bb3c9d8777527a2706
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45233212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cdc1c05c4a0bfedc3732c7313d16ea72e42c087cf7c2076e09a1cc6042329b6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Jul 2023 00:00:19 GMT
ADD file:20e9751a1ac7b1a4351d33fb8f1d9eafbfa0418af09f0f4dfac07e45c2dd03f1 in / 
# Fri, 28 Jul 2023 00:00:19 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:00:22 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:994d9244915c9e6508d8815d01ebde033ea2886f7b95198654dfdd8af2526b7c`  
		Last Modified: Fri, 28 Jul 2023 00:06:35 GMT  
		Size: 45.2 MB (45232988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58abaa9a96caf18c9eadc88d54ffe8f829e0eab6504a9641292a084b90830c6b`  
		Last Modified: Fri, 28 Jul 2023 00:06:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:c966441c35be33663da57899dc955a2511308738f5599b640c5a7c79b8736c49
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49591496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbacf007fdac8f4a168cf33cde8d318977ad371cdff6b678b9f12b59f02f8fa4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:44:16 GMT
ADD file:1685e9bd99067394420a349fe9fafbf6f0730ca2beeb3cd7f3f82c05ed20622c in / 
# Thu, 27 Jul 2023 23:44:17 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:44:19 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:41ef695b0dcdf6513df3775010b6de9dd5cf146356e0b22a0c8fb668f77acbce`  
		Last Modified: Thu, 27 Jul 2023 23:49:32 GMT  
		Size: 49.6 MB (49591274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e20c8daf04c1efdb68add453419155a1b15e7f2d6958004afd0e6ff83a8e76f`  
		Last Modified: Thu, 27 Jul 2023 23:49:40 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:0a8dc9b491a1e1fda1db1e4eb56a3ffc75ce80ed8b5a5839741655a5da8ae70e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50568050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e03eb5f7f62f32ce54402f7a78a6464ab2c67a8877654764be3695d120bd420`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:40:47 GMT
ADD file:c3f4390279546266e26e039791de6cfd53e464f4a08e3c352003596745bcd329 in / 
# Thu, 27 Jul 2023 23:40:48 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:40:50 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fb5312cfa75e3ad057b199cec5ef30dc0dc37843c2bba772372a61445f7e37c7`  
		Last Modified: Thu, 27 Jul 2023 23:47:08 GMT  
		Size: 50.6 MB (50567827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f217ad159c5a60494758e72ca2fd278c6ddad5cfd77f036af99cd8e3a347bb0`  
		Last Modified: Thu, 27 Jul 2023 23:47:16 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:07d61060db92b65e4efb917c9d04d12c827041bf8f13ad88b3dbe484ecc4e946
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49542274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062d57e3b04df6cc94bf1ea34d219d2886b1a63889639d8fbfb3304f598323be`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:15:34 GMT
ADD file:224ff2c2330e0b11d4a23e2914ed2a70e26830febc235424ef7e0f8010c3b882 in / 
# Thu, 27 Jul 2023 23:15:40 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:15:53 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9f78c9f83bb7be271c6dcfb95642a820bcdbb0fe6c6d7131806209e41f2c3dbf`  
		Last Modified: Thu, 27 Jul 2023 23:27:01 GMT  
		Size: 49.5 MB (49542048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9c0b0a2f467e113d3725888bbce936954d5cbc8b61e556177348cfeacb57a4`  
		Last Modified: Thu, 27 Jul 2023 23:27:12 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:4266eefbda56f2db624b5a262ab645daed940fdbae66f981a2ba794de864f9b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53543567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f3d92704f54b2eff654d6887a3a95cb216126d1323276a5c6ae685c2b5b9b7b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:09 GMT
ADD file:09c45999929f09514adf2cb9d6d0f0a57f4aacd62c4bd5ef96405b1588914a05 in / 
# Thu, 27 Jul 2023 23:25:12 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:25:16 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1d1be89ccee2abf523e50d302d1b9d4b49c822db5e4182c8f25dba9e0e2f1519`  
		Last Modified: Thu, 27 Jul 2023 23:32:43 GMT  
		Size: 53.5 MB (53543345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c001470affab71ef675f6cb32c77173fc0e763a84dc68d36f50005bd294174f3`  
		Last Modified: Thu, 27 Jul 2023 23:32:56 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:efb5567ea319dfaa95698d0bdbc727878f8c3703201b584a812bc382349df95d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47922241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d606c0cf86b23a06deef072f95876bd877c038b502c1dc71f06e608b4da62615`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:48:50 GMT
ADD file:9aafe828c01aed42f615a8cd6a088f7fd6616d528e4d91135828263f14d05eea in / 
# Thu, 27 Jul 2023 23:48:53 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:48:59 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3542e74447a7814dd3151a0c260f296bafad0b05dcd5d5812bf936180f6e9dbf`  
		Last Modified: Thu, 27 Jul 2023 23:53:48 GMT  
		Size: 47.9 MB (47922019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f33fefc1d9c8053992846f7b1e3569f5640424146fb296c09b5ec7236aeffc8`  
		Last Modified: Thu, 27 Jul 2023 23:53:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
