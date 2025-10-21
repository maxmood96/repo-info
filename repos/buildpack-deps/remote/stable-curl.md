## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:aaac53259d2197767f94576ec4e392a458904c43e41fdabe1b132dd43800fd74
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

### `buildpack-deps:stable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:cc3bb38a27dd3756e480447ecbc4e6db7b093cb504a89558a79041445239a2cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74899436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73cc89d451889952343ac9e9ceb8315bd5edeed687b9bd98828f193882fc5fe7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd090f42c4b7844c5846f9b4c719994f496fac3befe1d30f0ff20794e742370a`  
		Last Modified: Tue, 30 Sep 2025 03:17:21 GMT  
		Size: 25.6 MB (25614810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a835329e2a9b211ce7252783142431092ce87b628d8e6636a1a1310493d9e8fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4125919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247bcffbd240182b4a786d95ee1b3a5a9b19b76f0641e4cca68736ca2fa882ca`

```dockerfile
```

-	Layers:
	-	`sha256:162a104a8d05d3a5ecac91f55fa0a971dc563007eee3275437c8f91d66be549e`  
		Last Modified: Tue, 30 Sep 2025 20:48:39 GMT  
		Size: 4.1 MB (4118790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f99f0dec1161767f907cb872a028900dbdd00db8d94712624bfabfd1ee51e63`  
		Last Modified: Tue, 30 Sep 2025 20:48:40 GMT  
		Size: 7.1 KB (7129 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ab4fb8561a4d7aa4b08c02b5bba519319ccc1f651b0e6c14eaecdf1f29544e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71791318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab3770a69f428951037a1e00af8ef87f74769b2402b735deebb801d5a690fe1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:36e1dd9ce5730c29e323bfee77881b6b709a9ef3833ed3a509dabd626e23ef19`  
		Last Modified: Tue, 21 Oct 2025 00:20:35 GMT  
		Size: 47.4 MB (47448771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5aab8f083c99dfceb8649e1078e500b3226031e7fdab550eda596ce5b675db`  
		Last Modified: Tue, 21 Oct 2025 02:32:50 GMT  
		Size: 24.3 MB (24342547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b6fdbea62d66e125d567f472ce2e8562cf1ef3f3000358ff746261521d21d2df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4129035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8404eee75efdb302300cdebc2f127e7af8d1bb9fdebf615b3e021b42f42f0f`

```dockerfile
```

-	Layers:
	-	`sha256:a2d68415cb1859b075f1fdf0cbd36ab41748d021ae4aaff3a2f6405f5227ace2`  
		Last Modified: Tue, 21 Oct 2025 07:20:15 GMT  
		Size: 4.1 MB (4121834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3ce3ad2b99c1030e44551785f46a5fcca1609fd27bd544eb92a6488ebb93263`  
		Last Modified: Tue, 21 Oct 2025 07:20:16 GMT  
		Size: 7.2 KB (7201 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:88ee4bf9a5af96b6fa358994afda4c72ba83485871a60b8653fe3ef62b0ec561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69333156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38dd43dd1f8cfcf4bbc74f59176594d5f7190e87dee640296749cdbaaa5b101f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:25723cf5ae8b10c461d8c699bc5f9e41058f8fd5113212d106848ebe89fc0ffc`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 45.7 MB (45716494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452a743b80bee0c18e49576c93efcfb6c736c07dbdda0e38658362cec14c6415`  
		Last Modified: Tue, 21 Oct 2025 02:45:21 GMT  
		Size: 23.6 MB (23616662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2df55e9b842032366e757f9b726f1be21b270be4f9971cc15e309d5bf8e8dffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165d63596eb588ff131d4d86e5f7dd1a119bcba2d405d6ae7f05ead3512bd0f5`

```dockerfile
```

-	Layers:
	-	`sha256:18de0cab970bccee1530be2e820ab2b956311c90d2e2308d4a573d445e927855`  
		Last Modified: Tue, 21 Oct 2025 07:20:20 GMT  
		Size: 4.1 MB (4120345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b17821d20681cb41cea177cd0f1345261b67d363e6a027d34e0689a1858c46dd`  
		Last Modified: Tue, 21 Oct 2025 07:20:21 GMT  
		Size: 7.2 KB (7201 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3088a861393812b8eb498b253f3ee622a3f1d49fd679da9a6b4ce4452ecd1c2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74665065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d76d802e60a0493146a89d5020140379288b59442a68e739f16df73052528306`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:28aec8b14b3eeacbf47ef38af72fab694b109fdcdf31581722750599baf1a932`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003e6ed58c0c6ddbc757cdcbd876d66b9b5eed39128088a0055c819ebe15d20d`  
		Last Modified: Tue, 30 Sep 2025 00:14:22 GMT  
		Size: 25.0 MB (25016370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:36621539cdd2d2270a473ff121e3a3eba42320de61e5cbb2a4ef5b321a52a9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e397ea84f2529c65996550ee1cf119cc14403b8e279306660d8cb3a68a9cf34`

```dockerfile
```

-	Layers:
	-	`sha256:22beb0da5526060b7060ba6eafb423e4f439921467c8a887a5e7aeffc2da1c0b`  
		Last Modified: Tue, 30 Sep 2025 11:48:29 GMT  
		Size: 4.1 MB (4120332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea9e2ab573097d3003a25f792bb18f5b3b6d5bb42ea67fc57aa8c40b7a837a11`  
		Last Modified: Tue, 30 Sep 2025 11:48:30 GMT  
		Size: 7.2 KB (7221 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a894162646b9d47f4df858536071a2c1d67b64be5371d5b3c4a38e8cf13c741f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77574899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46b78407fb62bf54cfe8f2513541d7e29f68db994b3ef15787702a8c683108f0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f1c1f592b5569b5e2093c3107a48f2929b609f05af6d24c06d41a7ec1ae5e0e1`  
		Last Modified: Mon, 29 Sep 2025 23:35:36 GMT  
		Size: 50.8 MB (50800229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e5d861644e3a43dbea9917a86fd0d6ccf184bc7514ee58118ffa521ac4bc61`  
		Last Modified: Tue, 30 Sep 2025 00:21:14 GMT  
		Size: 26.8 MB (26774670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dfd46737f88b114a9a4b23105d85dae150f42c86ffab92262d4f8974ca15491d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61703b9071b9fc5be593d5ef6aad1949e31f3728373c56c64879c6590d9e5bb0`

```dockerfile
```

-	Layers:
	-	`sha256:83a4b7558b2032dd991a0c3168c40d896e359c1e2f6e2a7d31b901bc30601fe5`  
		Last Modified: Tue, 30 Sep 2025 15:26:12 GMT  
		Size: 4.1 MB (4115898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:074511d566e98b076b9953298e6e074716660e67ee7a19a831f1054238f229a8`  
		Last Modified: Tue, 30 Sep 2025 15:26:13 GMT  
		Size: 7.1 KB (7102 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ad355243a748fc6862477f6a8f5904c50d43637dafcb6435a4641d9af3ddbff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80104495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb18d56595787e0cdc1ab0bf23791d0655530ffeedfa8fdfd89fb88af497a155`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:71fbf24a239310917388930bb043e64907cb532b9ac8f265e44e032dc3bf4409`  
		Last Modified: Mon, 29 Sep 2025 23:41:05 GMT  
		Size: 53.1 MB (53109217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97a0b9869d194af98b70e095598cab3ab85032828ead695d63f75204d7418fc`  
		Last Modified: Tue, 30 Sep 2025 09:24:30 GMT  
		Size: 27.0 MB (26995278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ff8081364f07ec6e43572861305c49680fff01af1f868ecf1bb1900167f7599b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4129803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5317d7b388eca3e07fe9cf057ec0732d93de446477a9b492183c5899e8e2955b`

```dockerfile
```

-	Layers:
	-	`sha256:eb20a716e695145c54f2108c01478e0762e3160510e0d4c2128b7e5a7b03e63d`  
		Last Modified: Wed, 01 Oct 2025 20:24:48 GMT  
		Size: 4.1 MB (4122636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e75faf045abc8fea9975c404bd64abffa4d0d866eb722f754b891fd9a357890`  
		Last Modified: Wed, 01 Oct 2025 20:24:49 GMT  
		Size: 7.2 KB (7167 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:2cfa990c81e09c43e656b9d6f145d34f507e21872253d331b1662e64ca6afa47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72722792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ab260642d9cde854c53a79f1499debf1a2e0d8bab16ae554fd06dac687f932`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:913254a25f5e448a50a1e74fa50f037e22f85cfe4d6a3c626f4b7405299b7c1b`  
		Last Modified: Tue, 30 Sep 2025 01:03:38 GMT  
		Size: 47.8 MB (47770009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8533144b875d90b1f9c5a4ecb4c26177d9b646c254cea7d68fd43c77c27f975`  
		Last Modified: Wed, 01 Oct 2025 10:56:05 GMT  
		Size: 25.0 MB (24952783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d629947eae751b24520b238a0a88d3e17681ba028c6d264db74ab11baff6946a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4118467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:301d2fddefd1c97523bbd332585a9d161c7e83adf44ea592a287940be5e0230f`

```dockerfile
```

-	Layers:
	-	`sha256:1a65e19127282fe5839ddbd316d2eb1f0f4ea65f7516fe395120aa6fc4fdce19`  
		Last Modified: Wed, 01 Oct 2025 19:20:02 GMT  
		Size: 4.1 MB (4111300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d78ed77e964ded49a696ffe47357bac12576fa1e97380c660ef4a8ace4dd16c9`  
		Last Modified: Wed, 01 Oct 2025 19:20:03 GMT  
		Size: 7.2 KB (7167 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c92c6857c9f4de61b5e27dc603a2f77331b1c2534f0bea02d2395bf3dfd4396e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76133669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e760b1a03cd19d813d55e0b230629bfc86574ef97b3395a895bddda4d92e64fe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:024d6c344f0b9dbb2baf07e95dfd2abbfadc5c8262ca381f39f6489670cbaff5`  
		Last Modified: Mon, 29 Sep 2025 23:41:06 GMT  
		Size: 49.4 MB (49351442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae40148dca91a7d747a8331f403c812cb96e16b0e939c3f7e22eaed6bd4173a3`  
		Last Modified: Tue, 30 Sep 2025 09:36:14 GMT  
		Size: 26.8 MB (26782227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ed8547cf398b54007beb28d7eafc4a96c26ef61d225e5eb49eae91cbf9304d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf277632470e2a7195313d507f288564b57fc3c354db041d0f8542dbd62234e0`

```dockerfile
```

-	Layers:
	-	`sha256:41f15b252bb373d1fd995755510a67fe9e1264cbda5986325d9bc7fcf30c36f1`  
		Last Modified: Wed, 01 Oct 2025 01:30:28 GMT  
		Size: 4.1 MB (4120200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a0075ac4bb76540b272ce902a40b35529c7fc522f7509a41ebf0145b5fdb3d1`  
		Last Modified: Wed, 01 Oct 2025 01:30:28 GMT  
		Size: 7.1 KB (7129 bytes)  
		MIME: application/vnd.in-toto+json
