## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:76bc88c5fc39916a4809a287ed006bfd6f189814b962fd1f6bb28eb60dbdd7d0
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
$ docker pull debian@sha256:4dc65db8831e91d2e44265a46bb4f0b303d6571a022bcf47938fcfa59b6f0a79
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55058283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9610609813a7b933e84f0fa2cc2c19e7c41df4576a2b3c2f1c913f19db2dabd9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:36:07 GMT
ADD file:1765f92e3684fca356734b920648e551e9a8ddd5ea8ae721cb14bf6c19892e5f in / 
# Wed, 11 Oct 2023 18:36:07 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:36:11 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f9feb7b9924e141087f625ddd5fe7edcb3fa9edb01979a85f1eb52072679623d`  
		Last Modified: Wed, 11 Oct 2023 18:41:54 GMT  
		Size: 55.1 MB (55058059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2d53028d35c810957b54fd5ae2b3855537682509bd1d7b783fc31d89a1229a`  
		Last Modified: Wed, 11 Oct 2023 18:42:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:434160a4e353c6e2c523ce24aadc43af9a65f89fa64cf84e9dbbe0d8b6a35f11
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52563365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:951fc455f579d55b50ce4e9fb6a7ac2eb8d32366cd1b26f09fedf446bd4a17ac`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:38:06 GMT
ADD file:da1ec7816bb4779ff99eeaf749c3b64e98dbb058fb9b388970e70e6f0429ca30 in / 
# Wed, 11 Oct 2023 17:38:07 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 17:38:09 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:898468ed91f754fb929ec7597c79f49e3b926e76e037a02d099b5efc966c5435`  
		Last Modified: Wed, 11 Oct 2023 17:41:52 GMT  
		Size: 52.6 MB (52563140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4e68980b4aeb49b8ae7026ab17402966f4f0b0559121b1bd110c7d22f0a94b`  
		Last Modified: Wed, 11 Oct 2023 17:42:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:cd1ba5f77ca06712bfe9f0906e7d208e03e0e35131bba1dc15751780b5a2fd45
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50215953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee5b6cef0639f2ceecb0ad62bc975a5b3e041521e7e2e2df968947b5563bc44c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:43:15 GMT
ADD file:010bde6be30784c390d5138fd9cd7c469ad66c671eeefeb13c0e3c5186b70d86 in / 
# Wed, 11 Oct 2023 17:43:15 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 17:43:18 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cb4669bc4f8e091586991944d88167c76cb15c78accb55788140ac1b9b3250f9`  
		Last Modified: Wed, 11 Oct 2023 17:48:45 GMT  
		Size: 50.2 MB (50215725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e0032f4096be8d6bda80f0f95a994730169e3f77c407258cef3c93419431f7`  
		Last Modified: Wed, 11 Oct 2023 17:48:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:8fd4609e11ddcb83b24ed495e019fb95ce1aa2a20c3f155a0a5000e775b8145b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53708054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b11e48820af385a4bd7a70c028ce9bcd29cf7375256f9fa8fde3834ab4544a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:42 GMT
ADD file:3629f45242132f524ae9634afa36ea583bab2ffcb6ce49c842d92077add4c489 in / 
# Wed, 11 Oct 2023 18:25:42 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:25:45 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d1245b9fa820f4d2ddf78e7bad6329a51b3d8fdc1cceb450907259035c7e0473`  
		Last Modified: Wed, 11 Oct 2023 18:30:40 GMT  
		Size: 53.7 MB (53707827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe3116900dbf202b3a89d0a4d988a99bb3047b62e0aa3ed61625b4c02789c50`  
		Last Modified: Wed, 11 Oct 2023 18:30:48 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:ccffa478aab20cc8e8da61cdfe3993c7b72766e9cdefefd6c777930cb2d58cf9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56046559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:535940e9176c0ca78db707193f44884f84ffee522881f6df63179818787d91b6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:41:58 GMT
ADD file:fbb4026de842788be138f442c68c97c4cd9f05fbe7e282eb2a1bec5508f411c5 in / 
# Wed, 11 Oct 2023 17:41:59 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 17:42:02 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a4036d421c6eaaaaafb97abc75064e1210fdd67750a5efbda6e3aa357d14a344`  
		Last Modified: Wed, 11 Oct 2023 17:48:22 GMT  
		Size: 56.0 MB (56046332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e80f8954bd43ebf0e9403e42d04fdfcee8637ba2810f0c095aea1c5f54cd1ab6`  
		Last Modified: Wed, 11 Oct 2023 17:48:34 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:b6574b6d93136d6829fa35ac573a2b56466b986cdcc80b6b888e05c6e70e3215
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53289261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8021769bee64a371938659a9cc9397d00da3015118d74f9fc2c655caf0af9ec8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:51:24 GMT
ADD file:ffbea6ab30b7fadd815d53bb877e69b127714ea9976b06db2bc05bec98962215 in / 
# Wed, 11 Oct 2023 17:51:31 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 17:51:43 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e9dd1c85503ac6114304b94839ac51b6680fe86f0655e8a065dae67b6f39d32c`  
		Last Modified: Wed, 11 Oct 2023 18:02:50 GMT  
		Size: 53.3 MB (53289034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1260349e339ac2822ae504b7ab5a6b0a0dd90ebe629ab4b7884ddc5435527e36`  
		Last Modified: Wed, 11 Oct 2023 18:03:01 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:783b8b3d15434db7e4e3696fa129b7e301a4a7225654a4fb78c5fbc366f8c160
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58929953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0347e5dd70675504cff15050cd94b019a0d6ca9391784948ba1f269e62b706a7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:45:10 GMT
ADD file:47e58d18fb3653863b860db8f28b0e0be7ddb16ba79312033774149e613a2814 in / 
# Wed, 11 Oct 2023 17:45:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 17:45:17 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:425a16ca69e3109409f9fe8599a7e621808840c05aeddec98718a2a5a38c8258`  
		Last Modified: Wed, 11 Oct 2023 17:51:21 GMT  
		Size: 58.9 MB (58929726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8b071f6dacc738b58abac73af102a9a8d398625e8ad6ba6e5333cc671a9d9f`  
		Last Modified: Wed, 11 Oct 2023 17:51:33 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:17e12bff615831fa340bf347958bd1db78853cee18477d84b65e641f8246b198
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53296560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a63b3495b299326adc0a6f6f9bcc5ee2a9acbdec03d5e7cf42cfab1750dd55d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:51:11 GMT
ADD file:5c0693dfa39dd52d24f19239d55e43f0d2af245a32ae838ab8f32cf565c738e1 in / 
# Wed, 11 Oct 2023 17:51:15 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 17:51:21 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:035365d8ea846b3f48e8ae9876bee8e58e3af876d6745beefa24a3ab58db0c74`  
		Last Modified: Wed, 11 Oct 2023 17:58:08 GMT  
		Size: 53.3 MB (53296335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b185611ba09069c6e9b0d304aac44e6f29dc911fc62f50207afe932ab62adf25`  
		Last Modified: Wed, 11 Oct 2023 17:58:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
