## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:552b94353a3c7b095290a5101f4f1ee0abfbf73912030e7cc7722e1a9d963a24
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
$ docker pull buildpack-deps@sha256:730f6ef5b66e31d3fcd940a0de5cff1067af2630181ce25f7d14b52d2d79a8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71790024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ffcae249c1640037aa66cfde82e78fa0ff8e20a4794414a8396e0bd7825c75`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0096434708f67385cef0fbdd93979f2d8849a82842e1217f692977f3e6600333`  
		Last Modified: Mon, 29 Sep 2025 23:34:22 GMT  
		Size: 47.4 MB (47448480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a465ab5ce2f6d84d807e4534e3dcd0b62e1a1f4c158895b4c7b3539c651a1fd9`  
		Last Modified: Tue, 30 Sep 2025 01:01:28 GMT  
		Size: 24.3 MB (24341544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:995e148087c7cdd05af9e77cd41d522ac97867b4af326ac121707445420d8770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64e13868457f377ad5eb179ebdddfc687b737a103794637d8073a14faa22ff0`

```dockerfile
```

-	Layers:
	-	`sha256:494ecb97877480c7af21eeeed990f6bd5acbd7eaef4289f0389ab9e1795e57ab`  
		Last Modified: Tue, 30 Sep 2025 06:37:30 GMT  
		Size: 4.1 MB (4121780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85344fe1272444210cabef95e96c3836f7383a1f1f3e68adeb33648e70c0fb19`  
		Last Modified: Tue, 30 Sep 2025 06:37:31 GMT  
		Size: 7.2 KB (7201 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:770b14eea161a1e4baa51e19132762a716853375a89f79ea5ad6c4509e843d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69332013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa7c3b278d99753e12801195ca38ebba06eab59144199112ffeebb6554bf395`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2bfc3e00e130950b6362e6dfd7b2fb6422153e64a38bdcb425f69c089f79f4b2`  
		Last Modified: Mon, 29 Sep 2025 23:35:25 GMT  
		Size: 45.7 MB (45716141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b620f566f8b9a6ca407cd93d4d32d5e383b82be45b456055a87679d13e61cfd`  
		Last Modified: Tue, 30 Sep 2025 01:08:34 GMT  
		Size: 23.6 MB (23615872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cb619265dd7472843bab9eaae1047cce188edabc980053ba8ae50821fe4d7781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f2118ce7947f1f469aad8d56648568c8e0ef1ba6cd48232d82d00df08618d97`

```dockerfile
```

-	Layers:
	-	`sha256:8e67926aa27f477297fb2c1805520df974aa50e9d2929b5fb55149c42c16fdae`  
		Last Modified: Wed, 01 Oct 2025 22:20:22 GMT  
		Size: 4.1 MB (4120291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34dd0d6fb8e33c0a996dc75af6d41de672475415fc5b845a50989bbb6775c53f`  
		Last Modified: Wed, 01 Oct 2025 22:20:22 GMT  
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
