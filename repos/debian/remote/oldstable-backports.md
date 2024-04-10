## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:f3f2211fb6afe4acc9b6a036f1a83f112d62f3fe2034c1c2c913a4829d0cef43
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

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:aae4080c9f8c2219573452fc2012c8bb22e0e2457c42566bc00e16387218fd1a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55090512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7aca9f7719a1faab9d5249b30d97f06252d265902f7770e926cd147edc48d77`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:52:07 GMT
ADD file:1b437c2bbdd60b4bb66f629a5cb8179401f8e083d631fbf669ac17eb2cce1c0a in / 
# Wed, 10 Apr 2024 01:52:08 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:52:12 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:980d2c0fd652d1cf4537ce1fe45ebf9e0d9a2769f25545ec62d0a4f9a12975c2`  
		Last Modified: Wed, 10 Apr 2024 01:57:45 GMT  
		Size: 55.1 MB (55090285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454da4d87f5650a0df78dcb1b50042f72f1ffa659f145bafaddc1b7a3f7f63dc`  
		Last Modified: Wed, 10 Apr 2024 01:57:53 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:21d1ab3e5f2dbf8dee4a513e010c7f4a33ed3ced883b40db16d32d072bfb20cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52591883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca3ecd4f865c6f7b33ee4863e63d1aae5eea8a7fab32d2a18b4eb478ddc07f1c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:49:57 GMT
ADD file:a514ab7d7345b5312b8b0a4fcf78f0b4ad793b43268f6bf4a1b4a99d7b1f912d in / 
# Wed, 10 Apr 2024 00:49:58 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 00:50:05 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cfad491b0f309ee196806a01ac5d5e3bf70472652ee280fdcec9601cea45109e`  
		Last Modified: Wed, 10 Apr 2024 00:55:51 GMT  
		Size: 52.6 MB (52591657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c63f66bd9b82a111ad2ec48e263566d4144a7a0580a8bd18a884e50540663e3`  
		Last Modified: Wed, 10 Apr 2024 00:56:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:77092ac1452b0fc26d86195266b8654c54f8bea87a5fbf2b51b534a6ae3bb194
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50246677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a058b7d3d1c35d0095e6c651419e46688cbd27dee42a6f01b777734ee0906b99`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:00:00 GMT
ADD file:e61ecc3e656cfc321fc9b248be57e44d22d354a85153998c2c821ef696a735b8 in / 
# Wed, 10 Apr 2024 01:00:01 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:00:08 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:203ea083c11dd7781e27b1097c03c52d31bfd5b9f00e2cda6016b1719161c946`  
		Last Modified: Wed, 10 Apr 2024 01:06:59 GMT  
		Size: 50.2 MB (50246449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de12796d0cc54a919a89ee504e1373268e2d056512797d2d3321367867623d39`  
		Last Modified: Wed, 10 Apr 2024 01:07:09 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:99b5ee7ee3af4b4f9b1ce9ac39beb6798c084395ac29015278253131d23745d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53729381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fe12e6c31824d768818936b091128f29d6288ff10b5e7ec84baf2f021d6544`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:41:16 GMT
ADD file:53856f27805a92ba19246277ad1f99715b9ebb795b70d52c57c1ebdb2f2241de in / 
# Wed, 10 Apr 2024 00:41:16 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 00:41:19 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b94d92df6a8d1ebc18864a73e66c0f8447d12fd146762271805d17c1f59da96c`  
		Last Modified: Wed, 10 Apr 2024 00:46:18 GMT  
		Size: 53.7 MB (53729156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9615cf8f43bae91be79a1a6a7c6e36e7c9f8750f32b3a9e03e0e1bb5ee8a10`  
		Last Modified: Wed, 10 Apr 2024 00:46:26 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:d13fbd97d3fa5b1cae483cafc2513381615579679b4e470f0b71d07f77f05af4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56066376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce8ddedc4df4624e1cf9d18d61c79483ed56184ae476761e072509cd7ca08277`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:58:30 GMT
ADD file:bc59e69a699a7aeec26ef37e9838a8fa520f16f6ab2390f772b15bcd5d801acf in / 
# Wed, 10 Apr 2024 00:58:31 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 00:58:34 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c58ecbc6d2da373b1ff5004df926aeba03d2c87f0b7e5bb9996afe5d17e4b433`  
		Last Modified: Wed, 10 Apr 2024 01:04:42 GMT  
		Size: 56.1 MB (56066151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc718e0b044b9de5077f7eda0c4e1191802daae6245c07b9386843a39dcab13`  
		Last Modified: Wed, 10 Apr 2024 01:04:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:54392f9bf696b41e1d8452cbc17044c814049759ce53dc58fc973debaa72f5f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53310047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905529bd785771e8ace88be3dd651386a16cdf7ca85c6162dd3f2ac9dba115df`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:12:06 GMT
ADD file:ebf05b45f8ad0fa840802bf248bf8874fea1adf2474749f567f8cc9a4adbd91b in / 
# Wed, 10 Apr 2024 01:12:12 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:12:24 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:38d071e61b105895009e3f241f0d5435e58e52f5ed5741f737448caefc751b76`  
		Last Modified: Wed, 10 Apr 2024 01:24:07 GMT  
		Size: 53.3 MB (53309821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48240a1c2b4c3cda367c7ea98ef3ac0db22b3d8a99fa15afd7e6b53890e00518`  
		Last Modified: Wed, 10 Apr 2024 01:24:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:783203fbbb19bafaad764b234910a81eca88374b34f47e6fec8eecaea0ffa9c7
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58959236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b17e50a090ce9cc3f0d439077273263f11b9b2105aefe6885dfc8be85fdac51`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:27:12 GMT
ADD file:54a0a0763d477a4679ee4fa229071c803aeba6158d6e586caf741c772d52f208 in / 
# Wed, 10 Apr 2024 01:27:16 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:27:20 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:46df550798767a01529f5cdf1e9779b3249bdcaf4c5aa43ef424b99c57ca1acb`  
		Last Modified: Wed, 10 Apr 2024 01:32:23 GMT  
		Size: 59.0 MB (58959011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b678a24c9af184db058d5eae7ee90891b18e00488c61bd3785e58d44d3757c`  
		Last Modified: Wed, 10 Apr 2024 01:32:32 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:e5218a086e182f09109815639bcd4922c46c3e44196a03d28d76269c8720f09a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53325161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501cee80eaae42eab512d1886c828f806f07315f36551acaa7fe29ab9a3ef70f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:21:25 GMT
ADD file:3bfd973d21937ecce59e4b3ce776fadf15b3c108d296c5486cd6d66988f9cb75 in / 
# Wed, 10 Apr 2024 01:21:28 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:22:52 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bea9a17d2cf8a935c7693667f5bfef4c84899b938b7d45d5b2a069d3f03c49a7`  
		Last Modified: Wed, 10 Apr 2024 01:49:14 GMT  
		Size: 53.3 MB (53324935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa5a75a42d218acf8e663ac5330d366a4a5aa8f5bcee1fd960bb963c1989dbc`  
		Last Modified: Wed, 10 Apr 2024 01:49:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
