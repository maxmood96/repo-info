## `debian:rc-buggy`

```console
$ docker pull debian@sha256:8bec80f2199a4e4462bd7b5d01e810c9794a47da08d1b57d0789518291fc769c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:2fce59abaede589d306e8b1c4e204a71c6604a9c8a5867b8a75365da79ba7f81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48667152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f581197a6305118167cd120a86430708e12702ed483a0755cbe062b825616d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1771804800'
# Tue, 24 Feb 2026 18:52:15 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:d8aecb4bc7b9e58c615fe5a04f51a5710114ff668af7b4f56dd368d492375e7d`  
		Last Modified: Tue, 24 Feb 2026 18:43:47 GMT  
		Size: 48.7 MB (48666927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5fcf17ff0de00b48e81bca4d407a4504cd9d1119d560cf63668668b5b749f9`  
		Last Modified: Tue, 24 Feb 2026 18:52:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:d625eedd7c24fce5215e043e67e41ee93c14deb1df5023223ba2137731138627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3155159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed2c278291ae913a0e6fc9c934fc184e552e8b94d9dc6989069fdbdc7a8853a`

```dockerfile
```

-	Layers:
	-	`sha256:89eff4d6c382751f25b8ddb1ec7da8d5d75ee1f3c422c339ac84aa24318423df`  
		Last Modified: Tue, 24 Feb 2026 18:52:21 GMT  
		Size: 3.1 MB (3149103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e46d2b9b1880020fe7e2b8982e91ac9ed652ea40e983eae678b0d02fe55b5c5`  
		Last Modified: Tue, 24 Feb 2026 18:52:21 GMT  
		Size: 6.1 KB (6056 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:b636c4938d5835cd64a6e2b72d3058cdf4768567506787c8b7e151998ce77c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45650449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fabae689010af6b3e3dc8d9949d15af70da2796ba4f66126e3763bff15ebfb69`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1771804800'
# Tue, 24 Feb 2026 18:57:32 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:97ecb7dc5149349428e562613e6adb43b3de4d352c854673428e628da358370f`  
		Last Modified: Tue, 24 Feb 2026 18:42:32 GMT  
		Size: 45.7 MB (45650224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac53def95c26e08a3af1952f27878c2ad0488ad150c1641d3539938b370744ee`  
		Last Modified: Tue, 24 Feb 2026 18:57:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:d64bc0b393176b9543bbf15adbcc53b3843005088ca5f1b7b5d8facdb6ef17d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d86a03cb14027d17d07f884f99f585c3fbcdd484eeba958d4e89c141750bbbf`

```dockerfile
```

-	Layers:
	-	`sha256:aefba8908f4c68778a634b97428125a76c803b952454992eeaf874e9c505ce19`  
		Last Modified: Tue, 24 Feb 2026 18:57:38 GMT  
		Size: 3.2 MB (3150479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:525497ffff0b5da060f86e50ac865252b873739028e3eddd581dd7a61893b5af`  
		Last Modified: Tue, 24 Feb 2026 18:57:38 GMT  
		Size: 6.1 KB (6120 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:c512b7a4b5deea8265c7ea74e3e5a3cb4ea2f52049d3fbcc226a8ca1d197b34f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48709488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f2e1efae8e85bec206af9254fd3773d545008fecf6a746aac9bb056ea5b59d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1771804800'
# Tue, 24 Feb 2026 18:57:57 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:61a95a2f6784ce634817550699b53ea6f85b093ca9ec55f99c5217b534acfb51`  
		Last Modified: Tue, 24 Feb 2026 18:42:36 GMT  
		Size: 48.7 MB (48709262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0facc6a335714b7cf12b81eb1d4aaa60381117c279c14be2db6860c22539ef`  
		Last Modified: Tue, 24 Feb 2026 18:58:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:7702481ac68725b9bf2db14228f8de026c542a39664f44f32e51df39b7d02026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3162661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df0f8b6df5a4db6234c98b890154cd5ac61ff307ea1be371332586df57934bea`

```dockerfile
```

-	Layers:
	-	`sha256:d9b79974519a4e470a5e8847cdc65fb48fba2af1ff2987ea990ca12c15d17170`  
		Last Modified: Tue, 24 Feb 2026 18:58:03 GMT  
		Size: 3.2 MB (3156526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:296b96897c545975ccc24947d6574075ec9fc4134b5da2b46c3bb7fc46296a32`  
		Last Modified: Tue, 24 Feb 2026 18:58:03 GMT  
		Size: 6.1 KB (6135 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:811cfb19aeeb425b6d9341b6d9bbe263f373183c5e7fb491dee960046eebec68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50022340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f86a22aad937f62ece0b8e8168aeb4485b67a55770d276abb3c16fac8699f548`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1771804800'
# Tue, 24 Feb 2026 18:54:46 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:def456773a4aeca49d4b978ec8b12f148f201cb7cf9c2174e05e9ced13435b6d`  
		Last Modified: Tue, 24 Feb 2026 18:42:59 GMT  
		Size: 50.0 MB (50022115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fc545151be07307098151b86891c60270e1906e4406628c3ecaf0c840e325d`  
		Last Modified: Tue, 24 Feb 2026 18:54:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:014ac971d1608af63cc403e4a2203d65d5a93c1406ec2bf05b7458a660566e4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3152330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48fa9195ba083f0b5622d7e2f8d9b05a8b6e1a451e35c5b62cad91504d219e3`

```dockerfile
```

-	Layers:
	-	`sha256:1e38432b35d3a8ea174fa8fb77c79e384bf6d1700a1519f472ff6d41c441ce34`  
		Last Modified: Tue, 24 Feb 2026 18:54:52 GMT  
		Size: 3.1 MB (3146296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:916ce2a37c471a4192774248f1f538b6f016fc377ae819889391570fb0bd2f66`  
		Last Modified: Tue, 24 Feb 2026 18:54:52 GMT  
		Size: 6.0 KB (6034 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:c5dbe2dbfbea31a3f84867e39aacc4bf59b8f8191ef3ff1a91e5f5e68777cda7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53670428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1fa2eabe37d94fdb07cdc20333887e4155b0b60b0accccf769e4362a6104225`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1771804800'
# Tue, 24 Feb 2026 18:56:02 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:98cf99f8e5f75111e243f4d3c092140d6c7618c5cce72eba92c5c2c4d8f97f2a`  
		Last Modified: Tue, 24 Feb 2026 18:43:36 GMT  
		Size: 53.7 MB (53670202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d64505beeda7033b70061842a5a64dc407e6ee66dd5a2b6e2038b886624b6e0`  
		Last Modified: Tue, 24 Feb 2026 18:56:21 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:9e10428f227e00c4be339c589c9379089fd3e4735368ebe306145da446e8c274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3158712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1dfaf0dfec948ca4761b0359577ca0f8f267b118e1a7be173e7e46e78b9eb6`

```dockerfile
```

-	Layers:
	-	`sha256:68a644caa9205122c330c6aa37b7165097423e4eb29abd7173709dde5112450f`  
		Last Modified: Tue, 24 Feb 2026 18:56:22 GMT  
		Size: 3.2 MB (3152624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63308a3233a19cab3d724e897b31d1d44899d27057004f3a6a28fd0c5249c5cd`  
		Last Modified: Tue, 24 Feb 2026 18:56:21 GMT  
		Size: 6.1 KB (6088 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; riscv64

```console
$ docker pull debian@sha256:1bd4a8ec892954dade6e02753000715d684db48d97d844330d8206a1f6febf74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46910374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cfbee88a83b527dc9bb899b5ba01e30a911b5b9de617010c6ea74df5bc868ba`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1771804800'
# Tue, 24 Feb 2026 20:53:33 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:8883acc64dfc3047a79b0cc247a530d5064df45ee191c83ce50326e6f5321005`  
		Last Modified: Tue, 24 Feb 2026 18:46:58 GMT  
		Size: 46.9 MB (46910148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b127a200da351e5a7ae694e821678410783306fcb8dddac9c0079fcdd54be7f0`  
		Last Modified: Tue, 24 Feb 2026 20:54:27 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:5a9a7e1f488a27bc1c57260c1db9e137679e01ce82733f149304b124b7f4edb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3146707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff8ca6096f97dbfbf50c75d5cfd4733a211f2701b4da3fbc9fca68b7a725e18`

```dockerfile
```

-	Layers:
	-	`sha256:31b456f3f2921f775188429968bc1757e6ccdcefd4ebe3e3e0f2b6def7d9fc2e`  
		Last Modified: Tue, 24 Feb 2026 20:54:27 GMT  
		Size: 3.1 MB (3140619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41b0882f9672f753c4fc958a2213ab8230a9857c7612da8c8df2cfeef782fdee`  
		Last Modified: Tue, 24 Feb 2026 20:54:27 GMT  
		Size: 6.1 KB (6088 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:8343545899ebc0816d2647736fdf16c8a54e26bf54e9e09af897b5676e938bd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48447937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:108a7ed157d74e2f36e67c7427cdee7f0575853b78aa8a6f760590342cbccd8a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1771804800'
# Tue, 24 Feb 2026 18:53:58 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:b79b6ca78edd108b2b500a1c2abe8a5f5b6dee5dce46c5bd663b643e7c568362`  
		Last Modified: Tue, 24 Feb 2026 18:42:12 GMT  
		Size: 48.4 MB (48447710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c88750c6589736adf8de02d5c31f02805b1a07d18ae697ff6dc64b701a2c65`  
		Last Modified: Tue, 24 Feb 2026 18:54:13 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:816e956894bcbc7ba99a38d4113cc8d636957116fc5a14cbc89c79623de34a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32749a6cddac6e576f913109c2d1b7c2833e3181738a8dd7acc80a47590bf7a8`

```dockerfile
```

-	Layers:
	-	`sha256:f3e6f75adab29e1fbf534e820735dfc04445962b83fe1c90f9e2e06e859c3603`  
		Last Modified: Tue, 24 Feb 2026 18:54:14 GMT  
		Size: 3.2 MB (3150552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2afb1dcce4665e586616db01f69ee611997b9079a3db9a2268babfbb428ddb06`  
		Last Modified: Tue, 24 Feb 2026 18:54:13 GMT  
		Size: 6.1 KB (6056 bytes)  
		MIME: application/vnd.in-toto+json
