## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:30efcc449719630788d0b3bb5ccb34f5eb777ed8405cf363a03bf4835eb64728
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

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:c6cd809af904051227ab90f5fe831da3193a748002ad78a98bab4d5b91f27be5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55457359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16f48ca9acc0c85c4f5112ac60ed131debabb8c54fc110fb8af92ec83b6f58f5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:20:09 GMT
ADD file:601f6b8dd671536125813546a4e1c4a913eac9c0e1e5f1da23424c151afd0a86 in / 
# Wed, 17 Nov 2021 02:20:10 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:20:13 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2b2cd17dc00b5ed987bf109cf2a80e6f71bbc49808221e9ce4f632b0c3bf2cbf`  
		Last Modified: Wed, 17 Nov 2021 02:24:39 GMT  
		Size: 55.5 MB (55457132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aebc0444b2b5be1f26201f35a806a6698e6bcbb496872c02ef2a446451a745d`  
		Last Modified: Wed, 17 Nov 2021 02:24:48 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:f4b2523ae776542963c1784bc628c0ccce8448c0aae765bb0fdc4375100d9928
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (52954291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f3456ef5911d20a17d4a9f0e098e43d8bd6536b21431f366c5736e8830ed48`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:49:05 GMT
ADD file:60965734792efb0a8934b5931e629d56125bcc5c63c0c04e80182bf8a1bb8f76 in / 
# Wed, 17 Nov 2021 02:49:06 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:49:19 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4ac9e63a36c99e7be2a07d5f4e6656cfe302edce5271e79a0a75af86159241bc`  
		Last Modified: Wed, 17 Nov 2021 03:03:58 GMT  
		Size: 53.0 MB (52954065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d2bd641730534e6c1b857b7a8129274789d21a60bc0ea0715ce97d57f9f8476`  
		Last Modified: Wed, 17 Nov 2021 03:04:10 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:a12111d3107afe6e5cba6bd7284ad5fac71667d6ebe9a86f756011c9253065ee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50589242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58fda4853768dab32f5ea58f84d28ab2f888e02017edd6c19a217ad3c23d1fe1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 01:58:07 GMT
ADD file:6def097172b517cba3f58db99b3dfb25785929bad969e154025a1db5fce45c12 in / 
# Wed, 17 Nov 2021 01:58:09 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 01:58:21 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6316dbdb4f8715ca0987361e8e193aa4f97570b0b307991e95a5bd5475b35ccb`  
		Last Modified: Wed, 17 Nov 2021 02:13:14 GMT  
		Size: 50.6 MB (50589015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a593cabba4a80ac3c0d10f1ebf5685b08a5ed4cd93a935e5663efe65cad1874`  
		Last Modified: Wed, 17 Nov 2021 02:13:26 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:553a3ea7b9ef880c02121ded7674510c5d8849df4f3cf72101e5b6612779b0e6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54464614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7cc4f49d0f64481e618b845ce734645c1f9bb323be3496b196eddeda9d9a31f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:39:34 GMT
ADD file:cd982be7a5accd4c715a3de7a8682f869612c5401ec485ff4622a9590caf415e in / 
# Wed, 17 Nov 2021 02:39:34 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:39:40 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c646ef4eeacb8eade7583e3231bf320159c2c92b39835abd5631d8bcffea30b6`  
		Last Modified: Wed, 17 Nov 2021 02:45:59 GMT  
		Size: 54.5 MB (54464387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bcba5a68f6a2b8bcbf116fe8ea48697b964cd39cd77fe24a89c53d76f2d989`  
		Last Modified: Wed, 17 Nov 2021 02:46:10 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:e20eaae130866b755850bcd10c2286dea0808feb92243ac57e5cd82d7eb11766
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56490851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6dc1b7a2d435195ae6cadb7f718ac0caba4be936af78099afa87e1defad3e8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:39:06 GMT
ADD file:952f365b9933a7679a00c40feb459116dec4821f36ebbe7b93b86fe3db39e9a0 in / 
# Wed, 17 Nov 2021 02:39:06 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:39:14 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e4f07c4a13c97a4884800f77eed83407145089c45564213ae68f34cf4e49061d`  
		Last Modified: Wed, 17 Nov 2021 02:46:22 GMT  
		Size: 56.5 MB (56490626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e73ea4efdf59fe96473b744ae0d9bee91e614a9d4618bb3ef4a5fe8b54a114e`  
		Last Modified: Wed, 17 Nov 2021 02:46:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:becaa89cc62c033a5a51640af12896cc543d80532e487a3d5471a9f6b161eac5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54085908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2687a6a6698aa28b538f21cc026bcf40b3a709bd6b1945b3eea28c299dc647bf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:08:52 GMT
ADD file:30ef36b7192de64a1479731fca2ac7203d29511ecbb38732e0bcf5b572e8b5aa in / 
# Wed, 17 Nov 2021 02:08:53 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:09:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:76a3c406fc66bcc272351684f5b38ae64b35042b0075a004959ca5b74cacb50f`  
		Last Modified: Wed, 17 Nov 2021 02:17:02 GMT  
		Size: 54.1 MB (54085680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c3722bf0b9420a39cfe5a2435c3a4463d29169fec26b7b5a355eb9a2809e77`  
		Last Modified: Wed, 17 Nov 2021 02:17:12 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:cf22c84ccd8efdf50dd221507871231768c0cd98ff25dde3773f04eb348d0c73
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59660206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:718d2bbff060756f389eb0d469c78b30020375ed53c86d58f76e172f7e9338d1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:24:06 GMT
ADD file:2208d7bf60cb752ee46dc1a2c107f0ffefb15b83324ef516b1b93f03c5d0c249 in / 
# Tue, 12 Oct 2021 01:24:11 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:24:32 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3cb87628128232319961676d93044c80b66d2fba881080d5a34c710d8a09207d`  
		Last Modified: Tue, 12 Oct 2021 01:34:29 GMT  
		Size: 59.7 MB (59659978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8906c83d1be1e812c758a74046b16deb6646ed34f62abdf4756b9cb0017f04`  
		Last Modified: Tue, 12 Oct 2021 01:34:40 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:6b921b3ac95fa35d54bce79c71c521bb79945ce081dbb843ea590bcfaaa01352
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53669463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9a9322bbd38a47801edcbecc6975762fa99b8a17b3df5f0f0d24072a05ed03`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:41:36 GMT
ADD file:7913ed6a2385b3bfbd659a88c7bae1ef30f61c8147e8e89b5fc5c4be13a393ea in / 
# Wed, 17 Nov 2021 02:41:38 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:41:45 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4457396a5c3a0ebad221540b501d8baee17387a6ab52192d3b8f63e151492792`  
		Last Modified: Wed, 17 Nov 2021 02:47:34 GMT  
		Size: 53.7 MB (53669238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad19338e0216949f11a92dd8945b6e22f31f21cf795fc761001c8a74e348415b`  
		Last Modified: Wed, 17 Nov 2021 02:47:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
