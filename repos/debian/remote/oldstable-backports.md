## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:d9472fcdd066c41f05afdcb1308b90d75fbb417d72e7ece5492fa143caedae6c
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
$ docker pull debian@sha256:62a93a9e5b9b9b4109e05642be9b66bcfc5612208772e00ee58eb52ad879942f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53739097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c14b4fdf2849fc3d97a8316d67025bfdee6e6200214e282cd124d05a6415fcb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'oldstable' '@1738540800'
# Mon, 03 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:40716026d19424cb2ddd01bca241c8af8384eb91b6e4ae4c73a22f8a5403e71a`  
		Last Modified: Tue, 04 Feb 2025 05:24:01 GMT  
		Size: 53.7 MB (53738872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e9f72597ead7752b4361297d4a5c7d5f62d0f2b63357a51be774cdec099f7f`  
		Last Modified: Wed, 05 Feb 2025 22:19:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:98b143f9fc3d2b63484bf0adef114461f94a291ab5ef4a7f7c61b61cb52f2b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3923371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bda509803da8ab097b7799ce1a1eac5ffcdd32ba24f97b03e837e59bde4889e`

```dockerfile
```

-	Layers:
	-	`sha256:c5aa648a4f22c088c498f27a32253d7d3af102546b07366674c7759c02e3c4c3`  
		Last Modified: Tue, 04 Feb 2025 04:21:37 GMT  
		Size: 3.9 MB (3917518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54bbaed2b1fc1379d95f5d640d5625a7f2dcc7e28572fb1936d8a6241f7b2b70`  
		Last Modified: Tue, 04 Feb 2025 04:21:37 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:5cde9fb4a7559ee7ce9ead03e8c595122a0a970ea8e300e1cd809eec3ed0f040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49025020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f666c2bcd1784c842373378ef1ed1ab44d35445daf766b198ca5f4d3ab2b25e0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'oldstable' '@1738540800'
# Mon, 03 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:cea2f75499cae32347898e8f4a065c53c4227d86568443681c63362360402f51`  
		Last Modified: Thu, 13 Feb 2025 22:45:43 GMT  
		Size: 49.0 MB (49024795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe51b21de53a4562f97f0785b684b12eda2a81bea7a41a78c3010c88af2bdd46`  
		Last Modified: Tue, 04 Feb 2025 04:37:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9ebd0002dd0b2d196d7cd826cfcba4039cfef42b9de02d064ce20fe90173e23f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3924985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47e65acae5b25bb195c5e39151e895d60ee577e8b517dee5746028b047fa97f`

```dockerfile
```

-	Layers:
	-	`sha256:852c5feb9096082a94ba447db4ce9aba4812ff79a7e1b19bc4cb64b8a131205e`  
		Last Modified: Tue, 04 Feb 2025 04:37:51 GMT  
		Size: 3.9 MB (3919080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5030018c42775958891074d875cb156264b3946b62c027b89d99c8facca3015c`  
		Last Modified: Tue, 04 Feb 2025 04:37:51 GMT  
		Size: 5.9 KB (5905 bytes)  
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
		Last Modified: Tue, 04 Feb 2025 20:17:35 GMT  
		Size: 52.2 MB (52245694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24528d36f84ecc210aac2b949e5388392cc8aa5f9d9f46a94ff3ce26a862dcf`  
		Last Modified: Sat, 08 Feb 2025 22:45:22 GMT  
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
$ docker pull debian@sha256:4c66d3bbec24aa9e95e9f687ff36dba805ce72c31d274401afe0fe1ffd5ac38e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54676177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba1911072f7027116245c1e12e06b1b4845757c9e55392c53368ca879a2b8669`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'oldstable' '@1738540800'
# Mon, 03 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:58369cecd3b5ba01b57e1e0af2276a64ef17a6abeed4dcd9a41d3f325f6c0e46`  
		Last Modified: Tue, 04 Feb 2025 20:35:38 GMT  
		Size: 54.7 MB (54675952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589ac44f675d534f34fdfdb38a99646670c54b85bc04f06325d3f4cc97e2d59e`  
		Last Modified: Tue, 04 Feb 2025 04:21:57 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c8cf7722605e5664be8d9de8d87bdf40be00003cc1ecad2e4598f0a6ad685f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3919861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea5be7f29dac8c0339ad4d1a5252d5bc0e4587c055cf79c5e2f6a0e019ad9da`

```dockerfile
```

-	Layers:
	-	`sha256:74cbd6155c42472b11794f00e16125418fbb3545a2c1f61c16dfdf0838ab721d`  
		Last Modified: Tue, 04 Feb 2025 04:21:57 GMT  
		Size: 3.9 MB (3914025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3176e8e4a802b5dadfb2b45ba0036210c559a87159b0f54edd6c44b88417699`  
		Last Modified: Tue, 04 Feb 2025 04:21:57 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.in-toto+json
