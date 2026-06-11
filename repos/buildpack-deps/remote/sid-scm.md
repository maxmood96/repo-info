## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:cf7055b95105c7d53c919af7661cb30421be7d7ba1d66c36c2120f09237bff5e
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

### `buildpack-deps:sid-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:af93be6ba2d5967f155dfd30392997d1471048086a60c90c05dc291c9fc2e27b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154166819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5886ae2df81bf71ef152e409927cc06fdea5ee504f2fdc855d2bb815c6def8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:42:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:24:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bdd122fd70d19475cad994fa0bd624dc1524d2143c57c7c1f3f9e23fe40ddb0a`  
		Last Modified: Wed, 10 Jun 2026 23:40:10 GMT  
		Size: 48.8 MB (48801212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250af42f2a097a32d106444385fc18ff806e3b5890910b0e364be8e50256f63d`  
		Last Modified: Thu, 11 Jun 2026 00:42:46 GMT  
		Size: 27.9 MB (27921945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe07d3f4abc5d03b2d2858f1ba1c7420683bb86a466dddaaaedcbd7924b07e6`  
		Last Modified: Thu, 11 Jun 2026 02:25:02 GMT  
		Size: 77.4 MB (77443662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:db724fefa722d14a557c13bf4a02f31af470a84b4499931ed2cee05be39399dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8281015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7febb8938d887957a3d5082c2cd5c3438cfcf5ce630747e1718b54b2f30a8409`

```dockerfile
```

-	Layers:
	-	`sha256:55bd93da64deaccccacffb99655a3ec92eca5f00fba88b8084017ee40a226b0a`  
		Last Modified: Thu, 11 Jun 2026 02:25:00 GMT  
		Size: 8.3 MB (8273761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d5e3d2ff483cabab3d356471a8ef78d4f2662077e05b4c2c252296ce757f993`  
		Last Modified: Thu, 11 Jun 2026 02:25:00 GMT  
		Size: 7.3 KB (7254 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f8ac89738200886d788b6879bdeff6d1cd94aadcb6367565791c132b12df6512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.9 MB (142879024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c19cc369f2a979e60dc9051e40104923ae21678be520a0c7efe908a0b3c98c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 01:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6dddbc4e0b590efd809489171b20c0c05ae23facbf49b0dac491dc8f542364ec`  
		Last Modified: Wed, 10 Jun 2026 23:42:26 GMT  
		Size: 45.7 MB (45703240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86724da0b6362c0867d62fcf26f2b64559186172953570f5baa9b4fad9928363`  
		Last Modified: Thu, 11 Jun 2026 01:26:19 GMT  
		Size: 25.3 MB (25312845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db452c0bb423225c4a3bd143fc60d5a1dfd43be7a750053460623b4d219b8bbe`  
		Last Modified: Thu, 11 Jun 2026 02:44:48 GMT  
		Size: 71.9 MB (71862939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f014c0b26b468241a33d13e8823bddfa551f54e7993587c5913fc82a1b4c28ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8280984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d32896d0dd4caa0831d45780847e4805ab6125331e45ace3400cb9d917f515c`

```dockerfile
```

-	Layers:
	-	`sha256:03e62f9ac31d9737978d143e5b0171ea7a0f9c2c4693f87ddb9457a226e03cf7`  
		Last Modified: Thu, 11 Jun 2026 02:44:47 GMT  
		Size: 8.3 MB (8273666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6787a5d7eb96e07eebc966642c3910b9a1208f98c7d49cceee0c78451cd6abc0`  
		Last Modified: Thu, 11 Jun 2026 02:44:46 GMT  
		Size: 7.3 KB (7318 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cb997089799479c12c1dfff6c253cf826ecf6fecbdb5c0cedbd2fdb5cf3df7f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152514713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c03615789135e54d5759bcf7326a0adaf589b948792ea5de43c57032bd8661`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:44:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:015f4a5f6bd3bcaa5c5acf626b97030c3007c4b91e864c4cfabf1be5d52e7648`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 48.8 MB (48818557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bde100970346a8633eb293a95aaa718b901d789108bd4e63e4f66d9d3771ea`  
		Last Modified: Thu, 11 Jun 2026 00:44:23 GMT  
		Size: 27.1 MB (27124297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4cd7a68975013932751dfea9f2948b3d26def5e08e10b642c93f54033e1e2a`  
		Last Modified: Thu, 11 Jun 2026 02:25:15 GMT  
		Size: 76.6 MB (76571859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ef21c3691491bf6162e031ba5b45ee35d428918573f467038e2457eb5254e943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8292597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d910a72f6d048173827c660c94c3938e905f5a3a5e7b1585b2c334fa877f2577`

```dockerfile
```

-	Layers:
	-	`sha256:85b6e4955d8a0b6509650f346a9b2ed1fccfa62b8cd56b1769c9ae5f35885077`  
		Last Modified: Thu, 11 Jun 2026 02:25:13 GMT  
		Size: 8.3 MB (8285263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0557d79ddfbd7a6e98596b31782068a3ee4170b1873f4cbcd5a748e1c7e248f`  
		Last Modified: Thu, 11 Jun 2026 02:25:13 GMT  
		Size: 7.3 KB (7334 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:8e70a8ad9e08c462f901f37fe115d7d2bb59bf0c0fdbee02e07f672c845da66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158692897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e9febb40ee18dc48e8456a6ece5f2d9df3e805ebe55ab1e32cf77afafd23623`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:45:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:24:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a32252638de41825057387ef73b5d4de843fa9726fc243c76636da258263cc3f`  
		Last Modified: Wed, 10 Jun 2026 23:40:40 GMT  
		Size: 50.1 MB (50105399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6776bc9208fe6e23886fcebb117107385c0d62bb58b598a5be9aff86230bd6cf`  
		Last Modified: Thu, 11 Jun 2026 00:45:19 GMT  
		Size: 29.0 MB (29046245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3307963f270d1b61f7485c87a06ce39b78dcb16c03a58803cde22b17a8b7d56e`  
		Last Modified: Thu, 11 Jun 2026 02:25:11 GMT  
		Size: 79.5 MB (79541253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:33a6de8ca8a33793422d2f28262523bd436115b9a657c0fc25534dcf41a6498a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8276488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c44b3d15e31e540f79d67f7ffc31750be2ff933b15d07216ca55be4d322b9e`

```dockerfile
```

-	Layers:
	-	`sha256:c813b3c0e1fe72338671060421893385bd5b847a0e1eeeb2ee2fd7b1cbffacb2`  
		Last Modified: Thu, 11 Jun 2026 02:25:09 GMT  
		Size: 8.3 MB (8269256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cc3bbf4c38428e7b219d8abcf2102ec595585080f574e026074e89eafd09e92`  
		Last Modified: Thu, 11 Jun 2026 02:25:08 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6a5e2b30c7a4b91f7629880ad95dd4d860e9e350ce0ca15511f11fd001a71201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.2 MB (168234605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8fd016749ad1ff8f8ca98767c8c7203c41be5cfcf9cb32096a389b910b454b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 04:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 10:27:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1e0ce2460747d14df6cfd1da4b61c0c9b7caf034c9fddf19fabbcba65c2416ba`  
		Last Modified: Thu, 11 Jun 2026 00:23:09 GMT  
		Size: 54.1 MB (54132513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86f91ba1bf8c0d9e7dee82b12886a4f7ee70c339c3778c5cf99a230830c8d7b`  
		Last Modified: Thu, 11 Jun 2026 04:44:58 GMT  
		Size: 30.1 MB (30117465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a0b6bed36d53f6ece4654f5cea50eb41e560afbf8d24b742882a59a9592eec`  
		Last Modified: Thu, 11 Jun 2026 10:28:41 GMT  
		Size: 84.0 MB (83984627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:20674aac81672ea98ff47a36d451e39477dc7afe25812ef841d4c1582eaafe88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8262210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae1e07013c41fac64464c4bdd30f5344638d9815e832680b7166e15b2223bbf7`

```dockerfile
```

-	Layers:
	-	`sha256:15a8e2342c439e8e61963390a51cb03948d70e83f975b2b3c4992b991db5bc99`  
		Last Modified: Thu, 11 Jun 2026 10:28:38 GMT  
		Size: 8.3 MB (8254924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fe5f7903250a5abb330029727f1f043ff61f0205de5bfded645fe0eb10f3d95`  
		Last Modified: Thu, 11 Jun 2026 10:28:38 GMT  
		Size: 7.3 KB (7286 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:22be6b45b54e3bea750d71d6667c6edb5ba25405340d9fa5a2fa69bf9404ad4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148572654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fbdfec154dc690232ccac194fafbb378c00dec58870a841b144737334ebf5a6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1779062400'
# Thu, 21 May 2026 13:57:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 23 May 2026 06:41:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d609dbe8a64103ca9a52594c54358bca867134ca11c5bdbab5024849e5765438`  
		Last Modified: Tue, 19 May 2026 23:39:28 GMT  
		Size: 46.8 MB (46808398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9071891294e630f1468302f4618eeabbee9f63f74797f1ce63bdd2a40a26945`  
		Last Modified: Thu, 21 May 2026 13:59:23 GMT  
		Size: 26.5 MB (26450836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcb760ccbad4b8704448bd41cf7b9ae923800147ba7dbe24d29cd36600d159a`  
		Last Modified: Sat, 23 May 2026 06:45:23 GMT  
		Size: 75.3 MB (75313420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:88d441772ef5bd7f12f3549441c280eebdd1d9de331bc907e38c2883d2d01553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8260525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84bd9fa4b70746cfe5e0bf15a7c4b9fcfc9645b58b8b5733fdb492f9b3dea42b`

```dockerfile
```

-	Layers:
	-	`sha256:379294a33d056bc528b9c8e3e22de551b60e3170fba7b3c5bd1b359c7fc17043`  
		Last Modified: Sat, 23 May 2026 06:45:13 GMT  
		Size: 8.3 MB (8253240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d9599cd4fc5eeac997c83f282944e6a4e4626007da79a54c45921b39d60ea6c`  
		Last Modified: Sat, 23 May 2026 06:45:11 GMT  
		Size: 7.3 KB (7285 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9366d7b02278e58d885851fb163aecd509f95644c47d8e40450f0003867e23d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (154039557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb78956e1fb89e3b1a59fffcb2b2c065ed270fd0e0e4b4662996657063882c8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 01:44:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:26:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fb23912042361f66d2c3fed63550770682f92117280cb0cf2a2611ef14ea13e4`  
		Last Modified: Wed, 10 Jun 2026 23:41:42 GMT  
		Size: 48.5 MB (48541819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdb3735386433a0b206e3395692138596ad8486bc9cf1339bdb4dc651cae241`  
		Last Modified: Thu, 11 Jun 2026 01:44:48 GMT  
		Size: 27.5 MB (27516492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609c93fa43c64e99f6e508916e89876e16992649f171cc918b2100f0106656d2`  
		Last Modified: Thu, 11 Jun 2026 03:27:12 GMT  
		Size: 78.0 MB (77981246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:628cf6ca697e7f134582d9ccb5c4c1f615d507fc7c6c073031d8163672e1d2da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8255094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec990ac7ba1c7906a033e6e825e8f535de783ef1464ad0acd438779eade6897`

```dockerfile
```

-	Layers:
	-	`sha256:3d2d8ac0e9fbf33103a0c04a4fe1e675b2c1f9ae836a2e030e3940cfd85ef625`  
		Last Modified: Thu, 11 Jun 2026 03:27:10 GMT  
		Size: 8.2 MB (8247840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9516e9234dfa3de44801c69f52da1b1b8ae659172ff2a75e6aec308c0a59b554`  
		Last Modified: Thu, 11 Jun 2026 03:27:10 GMT  
		Size: 7.3 KB (7254 bytes)  
		MIME: application/vnd.in-toto+json
