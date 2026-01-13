## `clojure:temurin-11-tools-deps-1.12.4.1582-trixie`

```console
$ docker pull clojure@sha256:30bd2eddbc61c7a425f14673775b31286c947cf923c788f26050c1074315ee06
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.4.1582-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:68073f68d641bb69d35aad9bde7990fa9d004511bc3a6c514b98d206db6c0030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279799579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9078ee352c8188ca2b7dfaa997730d4430c927d69e7289b6b5c81253543b5a2e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:56:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:56:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:56:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:56:41 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 00:56:41 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:56:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 00:56:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 00:56:58 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:281b80c799ded5b9a390d2e8c59930db01ee395ab809dd34259897c660751f4e`  
		Last Modified: Mon, 29 Dec 2025 22:31:07 GMT  
		Size: 49.3 MB (49289587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e837d41a4eb898dfa75d7137c4ee9c524d3d23a675ef96779069b557dfe13e54`  
		Last Modified: Tue, 30 Dec 2025 00:57:41 GMT  
		Size: 145.0 MB (144966608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62730e7ab671eeb5664e6ca554aa01c1fbd4a5c9d210a846a75fc3f0c494c070`  
		Last Modified: Tue, 30 Dec 2025 00:57:35 GMT  
		Size: 85.5 MB (85542740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50389c739548009e15ede1b95c13271dff7c6da5b218a92263aed809d9b50bdc`  
		Last Modified: Tue, 30 Dec 2025 00:57:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1582-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0c0420d953b0be20a6bd03e7a9959cfd0ccbbd3d7c6cb73a21b23ec6ae50d8ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7501255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd04386d14407e631b9e7f9c9daff6ea2a23cca295def362ba509b0aac3d7aa0`

```dockerfile
```

-	Layers:
	-	`sha256:b1537cf773111c894cc56baedb7c366dd2983f31508ee98992dee739eb480502`  
		Last Modified: Tue, 30 Dec 2025 04:38:34 GMT  
		Size: 7.5 MB (7487070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7085855e566e89afda6ec2d532e6151fea8c51c6515d4aa8cd6c4287af5252c2`  
		Last Modified: Tue, 30 Dec 2025 04:38:37 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1582-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0aa0efec78c98d9e1c4ee95951b58f71ac0948dc3844aebd2f97b6c04c8fdcec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.7 MB (276743791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4778a95f8d2078ecb622f8b85e13698b810928526378e65c5ed224b64eda784`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:57:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:57:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:57:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:57:46 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 00:57:46 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:58:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 00:58:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 00:58:05 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5785abec2864dcd8d343ccd872458a50ffb2a61739bc46a79709c68c455cb8fc`  
		Last Modified: Mon, 29 Dec 2025 22:30:57 GMT  
		Size: 49.7 MB (49650193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78692600cca7ae534036f85abe371157893f258d4dce47b8612b11b472f4a208`  
		Last Modified: Tue, 30 Dec 2025 00:58:50 GMT  
		Size: 141.7 MB (141731577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecdd249dcaf8476f87994bd7fde0ae2a876c9075e58382082f5a6f45612ba919`  
		Last Modified: Tue, 30 Dec 2025 00:58:43 GMT  
		Size: 85.4 MB (85361376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b95e592f1dc18ad4f6eabb542e6a9e27ec4b9b2b5fb0840f302f5dc41928c41`  
		Last Modified: Tue, 30 Dec 2025 00:58:35 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1582-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:cb3a65ec93383f22315f36d86d4f5c4933e36bc1cb4814f4fb8dc2f59aad9552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7509019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dac2c8d7c6081cf2e1fbb043b10bf2b71f199c86e6a0461322dd10f430fa62e`

```dockerfile
```

-	Layers:
	-	`sha256:052a7e98943b47e8991ddf354fbcc0d45700afaf30e895a3057bb2d207b4e349`  
		Last Modified: Tue, 30 Dec 2025 04:38:42 GMT  
		Size: 7.5 MB (7494718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bf0e82c9f49598f7bdb70f0fe0af800b1569a1eee795bf68928311a4a9c07b5`  
		Last Modified: Tue, 30 Dec 2025 04:38:43 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1582-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:b1dde4031c95691b5ca32f790474f5734add6e4fe81fdebb7dc5784fa9c88a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.1 MB (276135957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a30f95184e5f76093500d6e587abfa9aaa05ed323751a98c3c7f1ac1b9b4046`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 05:15:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 05:15:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 05:15:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 05:15:55 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 05:15:55 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 05:18:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 05:18:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 05:18:35 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d586c84fb9377f9b3f4030e2c3e1e9ff7b1a23a68b8abc2c48a43163a3589257`  
		Last Modified: Tue, 30 Dec 2025 01:51:01 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac6c6730eaba1ceb02f2452db48e2462e345b11bc91b812b8459fa6340514af`  
		Last Modified: Tue, 30 Dec 2025 05:24:31 GMT  
		Size: 132.1 MB (132081947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeede58aa086ae5b25ae7e5d3f6da998f158a2f4d22822b033cdfde0b44fe30b`  
		Last Modified: Tue, 30 Dec 2025 05:19:35 GMT  
		Size: 90.9 MB (90944880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea9dc69fb518224131a57b680ff67199e2dc34606765cfc448fb6cbf8183cce`  
		Last Modified: Tue, 30 Dec 2025 05:19:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1582-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9f0536126b95d25bf9f55da68eb787957a59383873de9de9aff54fc9dc044c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7505107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb41edd8f31a33fe3fb88c739b9ee450b03639e646a082af229d41785590ea4`

```dockerfile
```

-	Layers:
	-	`sha256:7ac5c1501c81561aec5941cea0bc64ea6bbeebbc15994942d16d95c283c4ab05`  
		Last Modified: Tue, 30 Dec 2025 07:35:55 GMT  
		Size: 7.5 MB (7490874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d389173d01d422b5dc3c23b3f8f9fed52fd4c8dcc335c19f0207812cc88faf61`  
		Last Modified: Tue, 30 Dec 2025 07:35:56 GMT  
		Size: 14.2 KB (14233 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1582-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:96eccdc92824fdcd73169b3d08062e82d773957b900e7050738956b1407e8524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261552943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5063faabdfc61835f0fd8b008dcfda52d42d70ba236b9e6f9e0f042fcc02cd59`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:01:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:01:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:01:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:01:40 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:01:40 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:01:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:01:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:01:59 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9de0288d81a9602539c9f3015fc521191e25eebfe6442c22cb974ea3a486f3a8`  
		Last Modified: Tue, 13 Jan 2026 00:41:55 GMT  
		Size: 49.3 MB (49348704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff570185aa8ee762812b9a88c3c4d63d82c95867ee6119931614afe0cff6df6`  
		Last Modified: Tue, 13 Jan 2026 03:02:42 GMT  
		Size: 125.7 MB (125694469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f3d871e401c53f86af058a9e856f7ef8dba951cc6419f7205b38c89d7bec2d`  
		Last Modified: Tue, 13 Jan 2026 03:02:41 GMT  
		Size: 86.5 MB (86509126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152aa519e4c48b35b59f35149191e5e5c64c21e9e3091c2b8ec26ee0b5406931`  
		Last Modified: Tue, 13 Jan 2026 03:02:33 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1582-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f6ec68d7565e83968d731eedd40ea2527d27101d6a1bd4dcdce538313fa5955a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7498076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:601117c13a0da6438d34705c9c6bbfa6445dcd33da7e4f633a0a968b48b91d3c`

```dockerfile
```

-	Layers:
	-	`sha256:7e0b881435499a530587709f4f7964ad7ba4262ee734cb878743f9f2c48befcb`  
		Last Modified: Tue, 13 Jan 2026 04:37:01 GMT  
		Size: 7.5 MB (7483891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84926fde5c74248fd08c3fc5808a1c4dde04920a51253bffd1ff30bcfa37e801`  
		Last Modified: Tue, 13 Jan 2026 04:37:02 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json
