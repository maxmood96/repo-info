## `debian:experimental`

```console
$ docker pull debian@sha256:603ec22186819fc961f2465f27b4e5042e72e957d035476e6b70b08be9004c30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `debian:experimental` - linux; amd64

```console
$ docker pull debian@sha256:b279cc9c72c9fa3cf7e544f2ce727bb9bf8ce1038c85bc59f14788529aee7a07
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55702303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31fdaa2dc57071f1e17bda59e7fd5c9bd4575b5f15f22339a6ac7b84f5289f91`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:26:13 GMT
ADD file:d9d629780e76b855e899e172dd9c2c5af25041582089ee1b21e93ff0203a3521 in / 
# Tue, 28 Sep 2021 01:26:14 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 01:26:32 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:f2a8c55f290b62847a927b026f135fd01ab2550c4deb33fa1781c18f90374632`  
		Last Modified: Tue, 28 Sep 2021 01:33:49 GMT  
		Size: 55.7 MB (55702085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a6618546fc27afaf845d3034394cc0f15d38e1045cac3ae34bcce417a6ae678`  
		Last Modified: Tue, 28 Sep 2021 01:34:13 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v5

```console
$ docker pull debian@sha256:0a80e5feaef869d9e80bbf4cd7abf710f2a2d7987dbcfc6cf396a1bb18f2f104
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (52980345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47db9d8f2ce1034d197cbff322fc3b69b0e1b92a3a6708ce678ac37099a4fa4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 00:57:16 GMT
ADD file:35aeefda7cbfe52bd922da8352d6d36205e453c6a01b4910ead51a57fefcf7d3 in / 
# Fri, 03 Sep 2021 00:57:17 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 00:57:49 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:ca8098013e2d6d0f3902fecf5766117cb6127aaf3e4a072165bec0be91496740`  
		Last Modified: Fri, 03 Sep 2021 01:16:21 GMT  
		Size: 53.0 MB (52980122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef4f643165173ebb806bcc9a93f77dc42b48272a6a7e22ac5dc3f89bda3647d`  
		Last Modified: Fri, 03 Sep 2021 01:17:08 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:c7df2064f560eb970d0a6e538a367a2f4913d749dc1d61775c46610c8c6bce49
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50638101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a980063ea4a9aee6776f6336034ae5cb0985e08c9e660417502a6f9525d6c995`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:06:44 GMT
ADD file:bf59d647308e39808e127bfb478b359d6955717fa6a97c2c7a25d4bff031bb36 in / 
# Fri, 03 Sep 2021 01:06:45 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 01:07:17 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:48cda209034c6e805739dd1344fd37380f55e395e8cbcfb88881d7e80cce0cd1`  
		Last Modified: Fri, 03 Sep 2021 01:24:44 GMT  
		Size: 50.6 MB (50637878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55c00440b3dc92ccad515e84738d786919790de7d2fc4471bca6abb677c7301`  
		Last Modified: Fri, 03 Sep 2021 01:25:25 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:ffa74a7edf8c16771aa3e1e8af3d5eed4d24c30294faef70447e4b33931dd550
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54725540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b42c7c97535bf9e53241809cc92cc2ee42df0f24ab42d1f7bed7824a66e8740`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:44:06 GMT
ADD file:c6c834163255512247f4299caa0071f4b3fe9392b02ab3867c05508f08da5a03 in / 
# Tue, 28 Sep 2021 01:44:07 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 01:44:23 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:2d3594ced7745eb15a2b7007358597197a2ed8197194eae33fc3ea0db03f123f`  
		Last Modified: Tue, 28 Sep 2021 01:53:59 GMT  
		Size: 54.7 MB (54725321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666b3a15a5395971b6741d18737f616db4b8eebb644c0e355d1c2d22f4c81821`  
		Last Modified: Tue, 28 Sep 2021 01:54:25 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:c74b9a5b86929bf602240b6eb825c153181d6439af544dd0785bf56566f88012
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56733439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5410856927dbddda32c12d7806b55a3f365832967069630f6bb160dd032c0c8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:44:32 GMT
ADD file:6b060b0698e864f6ef8a07c3a6a71205dca18a95b9b8c95d64d2a2fdee7d7846 in / 
# Tue, 28 Sep 2021 01:44:33 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 01:44:52 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:9b5dc80bbd482cc8a27c804eb711f6f3216dcd2c0e78e2cdb9b847151d747ea9`  
		Last Modified: Tue, 28 Sep 2021 01:55:19 GMT  
		Size: 56.7 MB (56733217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2cc89fbb9e27513abfcf28343eefd536efaa49cd6b001560ae862aa0b02a23`  
		Last Modified: Tue, 28 Sep 2021 01:55:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; mips64le

```console
$ docker pull debian@sha256:2ed22c2d5401836f139b991a8854a9c7c57ff3f53e3a5663bd1983a1722cc4d6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54135244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d40ccd1286730ae8eb176aa590538c011b64aecba3e3557d03e998cd5607da80`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:14:31 GMT
ADD file:06b8e6c7631dd03ee95286f60728e93dfb5305af071b2a1de415e3b00f0b7566 in / 
# Fri, 03 Sep 2021 01:14:32 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 01:14:55 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:f9d6f94c6fc458ecc22830abf12c00aa2f763c4a38fae527558ce527081e5c41`  
		Last Modified: Fri, 03 Sep 2021 01:25:51 GMT  
		Size: 54.1 MB (54135022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0386d5291c708d9029e7e1f150f8ea82b06ae79c9f56e0587640cdee75f44d`  
		Last Modified: Fri, 03 Sep 2021 01:26:34 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:b77effeb230813d98019e468976c35c32cdae47c34288ca3c3f9f824f041bfdf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59534260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be868c8b2b7500d0ce91a7f829a42609e6d7298d8816f5aff36eea4a7316d879`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:29:00 GMT
ADD file:8a51a1c37e3e8707357ea465cbeb661f779abe15dd78177b507df7c4f379c897 in / 
# Fri, 03 Sep 2021 01:29:09 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 01:29:58 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:7997061ae42bdeebd52a682046b07a537363cce99bbd8e1a5a956bfd26232482`  
		Last Modified: Fri, 03 Sep 2021 01:49:26 GMT  
		Size: 59.5 MB (59534039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d5d123292116ecb7c8730a465d5ee07226ec12d896df03e1497f7e1ef75c084`  
		Last Modified: Fri, 03 Sep 2021 01:50:22 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; riscv64

```console
$ docker pull debian@sha256:2f9e2910e97f2f8bf6bcf98353c63a690b487472f8194a39725b6f39729fbc55
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51289309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44045f90bf5edd1432148a0f26dc9b197541a2dc4705c25d039c28905bfdc67d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:19:47 GMT
ADD file:3c786ac2e98158e7a24470ce33dfb8df0e24a7ab1702ac34cbb800f320c8744e in / 
# Fri, 03 Sep 2021 01:19:50 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 01:22:59 GMT
RUN echo 'deb http://deb.debian.org/debian-ports experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:f8fb8038fd63561c7012487a4a41109b5b2414eef638d69d26175cb04362653c`  
		Last Modified: Fri, 03 Sep 2021 01:36:05 GMT  
		Size: 51.3 MB (51289081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d9a67317214661414bc8708ec3c18456cf229ff064caa4fc6b48383c2532eb`  
		Last Modified: Fri, 03 Sep 2021 01:38:45 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:76a9aec81cbf2ff1cf52171e5a57fd696d2bc9a2601dfbbce0e85cce3d17ba2a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53954079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173c91a279f8fddd18831e4eda741ba964397b1fb423c6b4738a69715f8b3be1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:45:37 GMT
ADD file:8209381c87e3a9b971b314c7cb23655d9eaddd1cad08b612f6f6d0c97fa2fdc8 in / 
# Tue, 28 Sep 2021 01:45:40 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 01:45:57 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:95d1bea7bb30019c440a4a51393275efc64a586b9a0f916a69c27a386c444240`  
		Last Modified: Tue, 28 Sep 2021 01:51:40 GMT  
		Size: 54.0 MB (53953860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2ea63ed6a7e4e213858f4021cd6e8ae74db5bd9ad85c27ff53f739d566aa1a`  
		Last Modified: Tue, 28 Sep 2021 01:51:58 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
