## `debian:trixie-backports`

```console
$ docker pull debian@sha256:fbff03517a3a8106d535d224cc8950d69aab30c1b1b7b0086f53ec3101f0699b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
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

### `debian:trixie-backports` - linux; amd64

```console
$ docker pull debian@sha256:5843eecfda7ab4d06ff4c86b88890a636a18f45a2eac8390dba9a6259f3f1d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49254082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc8d980a0e3a5bff8a01ea8827c74ee769276ca38c554c66ab6e2c26bfc923ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d8e51f6b7dcdaee60f07f9a13a971abe1be9dc977d52d0849087118f80a1c7d6`  
		Last Modified: Tue, 10 Jun 2025 23:25:45 GMT  
		Size: 49.3 MB (49253859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4127c7dd0c0eb60c47e7862bb538665715f9409a91f59b2a44e2cb2dbc64327e`  
		Last Modified: Tue, 10 Jun 2025 23:26:25 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f85aa6d9a13939a17531f824fc82ebfadf160b8dbc496add729a9900c0a1bcf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3173663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a356117d065f8cbbae892d12690aa828b9163c1057da0352b952aac0a7d7bbf`

```dockerfile
```

-	Layers:
	-	`sha256:c0f26519e38c1d37d37c023265e32c50ca52e6a00d354fdddea42ef0d01b0696`  
		Last Modified: Wed, 11 Jun 2025 00:30:10 GMT  
		Size: 3.2 MB (3167836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b06c68ac969433b89a3d237c05042c2701515146ba79329f1d1e2f07b517c694`  
		Last Modified: Wed, 11 Jun 2025 00:30:11 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:c3288c243839dde00a19c6078b0e4b7c97d21b15790899f1dfcb17d0df1cb351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47435724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df17a986121d7190895a6866741243b74417ba819f6cb6234a47eadce6cfeff`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8c456e7e2a39b691845cb9954fe5483a7f4a7e63934a177c56842196d0ce4501`  
		Last Modified: Tue, 01 Jul 2025 01:17:08 GMT  
		Size: 47.4 MB (47435500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944b1518a84daa0bcf33ea9cb7349454e045438d5ca02a8ceb7fc95c03a9145b`  
		Last Modified: Tue, 01 Jul 2025 02:13:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4a861f5c9fbde6be65a7732ba3ac4381e1a7c6a5a53df8ba232a27550dbc6fae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3185909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37bee60ffae018fde34429e50a3fcfdd7cd2cf12b309bfea03b2d293c0efd120`

```dockerfile
```

-	Layers:
	-	`sha256:0ac3e64397a4a0b5c62b27108da6347aef2c4058f435616015c4eb55ad1f28dd`  
		Last Modified: Tue, 01 Jul 2025 03:29:48 GMT  
		Size: 3.2 MB (3180030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f5b8b7318f801b2ca7bc8420452c1f6c31cd7baeffd5a910974efa7a27f743e`  
		Last Modified: Tue, 01 Jul 2025 03:29:49 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:3c21affba29624d5eb8d2bfada7ad2bbebf33b5fcab6b7efdfc27a82c186cad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45708303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fdf24b5d4066a1c50fde5ff1e5728fff95372674144b7157cbc005f7d07bb51`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0611a9c58dddfe7f00bb5fe6c8f5ccecfceeb1785acc68dc070068a94adf2092`  
		Last Modified: Tue, 01 Jul 2025 01:18:31 GMT  
		Size: 45.7 MB (45708080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce55d02afd16ffd8b3f4b0076ad1f4a466efd4166723fd44e51d7c0b4bb3e60e`  
		Last Modified: Tue, 01 Jul 2025 02:14:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:009e207e2439fdaee364d5bc7ebd9181045c40f6873c1dcb0be0fe10e357be6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c75a09daab2b684abdfdbd1701696ae21fe0c8b8962b85b6902ce661f029c25b`

```dockerfile
```

-	Layers:
	-	`sha256:001e738c068ec29cc0d384d68fa45eb32c6bce8d4d0664b17c05e965f63931da`  
		Last Modified: Tue, 01 Jul 2025 03:29:53 GMT  
		Size: 3.2 MB (3169214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5021444c5ca01977f920023a56a6d6c3bc49933f0195403acb33430cfd1ddb65`  
		Last Modified: Tue, 01 Jul 2025 03:29:53 GMT  
		Size: 5.9 KB (5878 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:ce5ca7d9be55f94e2f0312652afda2cd716f5143296625aed8b372990c8c4b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49630377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bde30c4de20b96136ab3b52c4e6fa052f7e55aa3cbff9b4dfff4eff91fd307`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2581a046e315a4b3013d50a17da46bcffbba144014a55d733fa55c3bafc6b7ab`  
		Last Modified: Tue, 01 Jul 2025 01:18:05 GMT  
		Size: 49.6 MB (49630154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7c9dbc93a3f9b8fea01f416660c86ff9bb278494a746ddd6246cc5852ed942`  
		Last Modified: Tue, 01 Jul 2025 02:13:35 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:96d8e9606bd763e5028a0fa5321af41052c0dff969f3ac390c298f21a0620ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c63c2042538b11d9f40e46eaa91406f51293abe559680be576ff223aedd60a`

```dockerfile
```

-	Layers:
	-	`sha256:f3c4d2c5bb0117cf176605af4cfb343904277936ce5409329386d409ef17df00`  
		Last Modified: Tue, 01 Jul 2025 03:29:57 GMT  
		Size: 3.2 MB (3169321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:577fe19929e01c8f7de35616ece217772d36127aed3c6c232d4908463ba91b1f`  
		Last Modified: Tue, 01 Jul 2025 03:29:58 GMT  
		Size: 5.9 KB (5895 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:91d9e197739bcfc905ea9f2aa3b5c95019e0f2495464086ff13a65354cb69c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50786980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cabf5f63974734adac6c1b768766314831e2accc7b3558b54bb2191e3fc3b0bb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d223755a7489df8352d3a71955e26d35281b9c0f0609e017af54d9e75e3b435b`  
		Last Modified: Tue, 01 Jul 2025 01:14:59 GMT  
		Size: 50.8 MB (50786756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7b2b8183484470fe0f11ec9c3666c05e8d5d4b685b588ec9d0752b7f982d65`  
		Last Modified: Tue, 01 Jul 2025 02:12:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b8e1fc2873a86b5d0ad004502ad48c25480ef7cd65ace624690974a41432b31e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3170854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e221d46423183d20ee73c81abd9a9e507c577a10c4e17928d6aaabd0c5e0a8`

```dockerfile
```

-	Layers:
	-	`sha256:f13b83170b462ae231a9bdcbadbd640d268fb682c8d58daaadc59c3c14589f0b`  
		Last Modified: Tue, 01 Jul 2025 03:30:02 GMT  
		Size: 3.2 MB (3165044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2619ef9abe1e8965ae2e496403ecfb152278fbf7123d2a3e7d589bdca83590e4`  
		Last Modified: Tue, 01 Jul 2025 03:30:03 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:4c6e037cb34e211c0aa958b1c5e5e14335da10cce1b16b1381e3c37c2bbcade8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53097460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982bb0bd88423c854d153ed06ed0a58b179249203a346c859c6a3e2219c4170d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5c6a246a80c20351fe842a314b6b3f8561a5ceaea736decf36fe380b29e53224`  
		Last Modified: Tue, 01 Jul 2025 01:18:57 GMT  
		Size: 53.1 MB (53097236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5406ba1ac2a14916d5dfe3bed6cdbe441e4d8bca698505fa7caa4c099b1cd6dc`  
		Last Modified: Tue, 01 Jul 2025 02:14:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:82481d8f5eecaccd8f54215e6ecf5bcd6828743ec92c860f71c7fdbe4b358ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3186455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e65ba58f4317943ffc0817fa51326f7977c60b498e10f36309a45767507a4486`

```dockerfile
```

-	Layers:
	-	`sha256:ef60bd2509cf16b7a7e835b7066f92168b267a653c2eaf59de47d02d65e27e53`  
		Last Modified: Tue, 01 Jul 2025 03:30:07 GMT  
		Size: 3.2 MB (3180602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17098c2ea5087e639e30e7bd9ee12491b0af6ead9e57dcbf78cf9438d0a03610`  
		Last Modified: Tue, 01 Jul 2025 03:30:08 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; riscv64

```console
$ docker pull debian@sha256:6db67d0741eef19cb91c731ed1991f76331150cac62bb1bf7c7e8ab087851fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47750382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6177008e0d499503293258b7ba9a6815afedbb3222e76d38a28bfba2582cc1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a19cda6d0aca0ae93b23898ddaa4518ab5077c7011f945c7a7e4a2cacb08ca5f`  
		Last Modified: Tue, 01 Jul 2025 01:23:18 GMT  
		Size: 47.8 MB (47750158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d080926ffdfd68875ee2220962741984d1bcba323d00a18ddb22cff663b59f5a`  
		Last Modified: Tue, 01 Jul 2025 02:15:59 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:75aa107ed82190073e8caa0afc7b2e1d29a1aeed1c7ab8e0fb78588e8f526c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3166014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d49aa733ad340d1b8738404a0297b1ddd964d22ad7591bad74a4d98ce157c8d9`

```dockerfile
```

-	Layers:
	-	`sha256:311c47d86ee0926d4127275110e427078784b64453687d7a35c7e99fdaa643b0`  
		Last Modified: Tue, 01 Jul 2025 03:30:12 GMT  
		Size: 3.2 MB (3160161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c803dd2ef1708360d115ab076b4cca094311052f4b3a9dc6733f3ade1d6c206`  
		Last Modified: Tue, 01 Jul 2025 03:30:12 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:417e2e2be87b0cb20d5d1c90c1a883ac36cd2e397959156d83b3e6cd88830145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49343883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2109bfb31fff1aa734483f6249713dea3a0fcca621493bd5ede7220dd9ddb84`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:48de1d8f52c0a2a00375babc11bf69628b8225862d3b6ebbb2205e4ae2f3e96a`  
		Last Modified: Tue, 01 Jul 2025 01:19:00 GMT  
		Size: 49.3 MB (49343660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9b01f74d55b1ed5402ae33817ccd0b4ee5e6018f24ff0ce8cc2f1958c15b48`  
		Last Modified: Tue, 01 Jul 2025 02:13:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c0c7f8704826669e187fb26c9177c1e71a70b2b1ed5591c58e317281cb6bc097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3184367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3b544ac4607b45c6114869d81db859acff52add967357e106453caf9af4628`

```dockerfile
```

-	Layers:
	-	`sha256:8577f5f4aefc5bd422bf73e9a7da5e7d81b2be0a9f713f3b7422cd7793bc0406`  
		Last Modified: Tue, 01 Jul 2025 03:30:17 GMT  
		Size: 3.2 MB (3178540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:400d9f3131ee2a01620d9df74000432ed9cfa3a621a68cd51d32e5b6db9ad45a`  
		Last Modified: Tue, 01 Jul 2025 03:30:17 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json
