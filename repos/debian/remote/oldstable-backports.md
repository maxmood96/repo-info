## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:518c4ff666d122c351368fba892ac65e7388d1b3fb68d2e46af0d3387e123dc6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:c9e03eeb727b9e20a595ad356b275a634ec991aee214ee5482736196065119b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53741621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c827407f1296b7770024f6004d47ba5ae8634dba85bc0755ef8ea67d461e31c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'oldstable' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1c1bb87b23cc30a6c7d26e68d050c8fc458e6bda092afaf2ee868dc1b489026f`  
		Last Modified: Tue, 25 Feb 2025 01:29:48 GMT  
		Size: 53.7 MB (53741398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1699a25d2fa3bd1d16d94115f3e69fbfae62d18fe3e23cd4c9c0ac4d5ab400d2`  
		Last Modified: Tue, 25 Feb 2025 02:11:51 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:230909b3b7e7fffd0f02a762bb7eeebd7b6d44e02ffa52ab316bbeb14c17a23d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3923371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0ddb482fedee753e1711b3e1c9b4b7da886059ac7252f4d316fb0c60cf1db7`

```dockerfile
```

-	Layers:
	-	`sha256:9128ebd8f8a6198536b5f255e06346db99a393e3ee6e3542da193aea1845456f`  
		Last Modified: Tue, 25 Feb 2025 02:11:52 GMT  
		Size: 3.9 MB (3917518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b5156eb298bce1e69d1203a6843d4f5e1226f864e43cfb35d08e2c696544d65`  
		Last Modified: Tue, 25 Feb 2025 02:11:51 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:895ac53d43613544e12fd7098844785274dc3c3e0540c5f556d64b95b20b5d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49026959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfaa715b18f1802069aedee14859882e8b3e0a57018aa620adedd775db2a659f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'oldstable' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:41b3c0e18c9315651c24575105ca09b81f294c7cf69c17c2f9fe94fc342d706b`  
		Last Modified: Tue, 25 Feb 2025 01:31:40 GMT  
		Size: 49.0 MB (49026736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c283c3391caab77b639b1b82fbf262a4800241a5827e231cd9651fc9ca06eaad`  
		Last Modified: Tue, 25 Feb 2025 02:16:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d23ee1fa4a52c73f4986c9400cc3c1a8d6c3dfde1b6f835770b74171d978ef9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3924984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423e08ea9aafa234c9dc9609dbe1ae546728b6d80a713d63e2600a4313d46cd4`

```dockerfile
```

-	Layers:
	-	`sha256:5b9c5e141269beecc338b028eee831dfb847283ae108a8bcc2125a974538914b`  
		Last Modified: Tue, 25 Feb 2025 02:16:03 GMT  
		Size: 3.9 MB (3919080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9c844ff487c6d19edb056c7748707ff2d2bc611cb5690b570c9dd0a7cc8b12a`  
		Last Modified: Tue, 25 Feb 2025 02:16:03 GMT  
		Size: 5.9 KB (5904 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:a24059210a05e894ddf9731c54d2aff6286646bc5c17be496967315eb3998fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52245917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e85247f12f5fa2ecfe114133faf0716068653e26ec4dc5572bf6c2c1560aff`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'oldstable' '@1738540800'
# Mon, 03 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:937db6ef0aa4d3bc4706e733560e60b71c45d34caa084e212a3d027196898d81`  
		Last Modified: Tue, 04 Feb 2025 01:38:42 GMT  
		Size: 52.2 MB (52245694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24528d36f84ecc210aac2b949e5388392cc8aa5f9d9f46a94ff3ce26a862dcf`  
		Last Modified: Tue, 04 Feb 2025 04:29:51 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d0f4f69149d61d63bb71bc09855d563616f6893812c1adfbf80488ff61a37443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3923018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:794e8f7a2d6e44afb8a52e2764737fe0b819fc77947167e4522d22100a99785f`

```dockerfile
```

-	Layers:
	-	`sha256:5f06bdd8888e8796903f78dfad3031445349db494e77b3a8945e1c0a82f0805f`  
		Last Modified: Tue, 04 Feb 2025 04:29:51 GMT  
		Size: 3.9 MB (3917098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45ddfbafd279a013b96a90163613fa2bbaf6093bb8f46d564ea6507d1e8d5c47`  
		Last Modified: Tue, 04 Feb 2025 04:29:51 GMT  
		Size: 5.9 KB (5920 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:51983274e7f013eb31267bbc53a015d00b62614c007f540c33a38cbb36ed257a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54679087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a53aa99a0ed72f47c2f1f15a361ec33d951f68df95f353f5c88438fbc01d096f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'oldstable' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:138cdba7209ad46195ed6e116e147f9f45af753159c64d76eb1cc150b39a53d5`  
		Last Modified: Tue, 25 Feb 2025 01:29:55 GMT  
		Size: 54.7 MB (54678865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba2525e96fdd65b5318efb3485ebc58a2d32cc3757ff570f99078d1d99030c7`  
		Last Modified: Tue, 25 Feb 2025 02:11:18 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a27ecd4bd93b7f63d8525e33eafe21b388a31f27cede1d6f8ee7eb3b78fdb69b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3919861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1c09b479785ec32b237c0dab636e6f5bc5166d88d1aa2b9e0f1d6a3b569e1d`

```dockerfile
```

-	Layers:
	-	`sha256:18a2c45675a03d1f298b84600837f641964e17a90f0bfb939be5b52d94bdf56d`  
		Last Modified: Tue, 25 Feb 2025 02:11:19 GMT  
		Size: 3.9 MB (3914025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c990ccd38fc0dc0091e3ee1200a7a69c26a1befb77115f6c0bbb3afdaa6cb74`  
		Last Modified: Tue, 25 Feb 2025 02:11:18 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.in-toto+json
