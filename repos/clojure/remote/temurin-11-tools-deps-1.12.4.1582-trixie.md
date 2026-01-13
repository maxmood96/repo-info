## `clojure:temurin-11-tools-deps-1.12.4.1582-trixie`

```console
$ docker pull clojure@sha256:7af7bc4f054336b55cf6eb22180ab345d8bca81f02388abd74e27730d4f8f5ba
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
$ docker pull clojure@sha256:26b6843d25d4115d613ae5fc8db4be61c333f8266d22d47f49826e7622150e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279795916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c4607691cc37ea3b9c02cec2e95d2a803625eafc51888c28e7fa081b13f282`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:25:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:25:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:25:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:25:18 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:25:18 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:28:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:28:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:28:58 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e78e7bb435066daae0345d54d76378d787c55f699b77d975f071f5a7cc2f39`  
		Last Modified: Tue, 13 Jan 2026 03:32:51 GMT  
		Size: 145.0 MB (144966652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35072f59c30c05784a1b399d5ba8e03007ef492c56675721229136a9577bd9d7`  
		Last Modified: Tue, 13 Jan 2026 03:29:27 GMT  
		Size: 85.5 MB (85542998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813845a00fb6ddc8b9e9be709f2b532b80ed21806cc805f6518104a5c81cac8d`  
		Last Modified: Tue, 13 Jan 2026 03:29:22 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1582-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ccd2f39852e0264c30a80f89d94ee541d21aa4293be4b49bc45808c7b4f424a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7501349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de65cdfe9378af0ccb8f8471fc120e24b39e9ac32c05dbe68b474bf7bbe60f04`

```dockerfile
```

-	Layers:
	-	`sha256:5c4932b94be18c19613fd710e7ea3217a132ae75e7e2e78523035ffa9e452fbf`  
		Last Modified: Tue, 13 Jan 2026 07:38:34 GMT  
		Size: 7.5 MB (7487965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:913ed6b447077895b972174a024eb5e64aad2fd579e39dd3dc9fb41c39013b84`  
		Last Modified: Tue, 13 Jan 2026 07:38:35 GMT  
		Size: 13.4 KB (13384 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1582-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:49d23feb7d6f7b59f5182765026282fd1e7da910a39ff8d5b421128a41f10e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.7 MB (276741444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:853575d4c677a48bb7d7a4a4765c08c5ab4bc71ec7ada4e21e00ca2471537aa3`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:32:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:32:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:32:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:32:27 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:32:27 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:32:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:32:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:32:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a802f438e9d6c0bcf1d99c69eec309dd0acdef6daf093a59a061f977a82d98`  
		Last Modified: Tue, 13 Jan 2026 03:34:24 GMT  
		Size: 141.7 MB (141731552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73a8fbbc312309ffb7d836a01f2f818d8e2941de6da5c413d953b97eb48e976`  
		Last Modified: Tue, 13 Jan 2026 03:33:25 GMT  
		Size: 85.4 MB (85361165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b453c8041ce09963f3541c9ea2c98b5993de5a9bc38003d868ee02bc4192c1d5`  
		Last Modified: Tue, 13 Jan 2026 03:33:18 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1582-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9048d52072da17e23565f6ca31cc6c61c1507dfa228a93f8ed208caf983a7ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7509916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3d569fe7632bd327bec97efdf2f229e78406ba3baad3b7f2b3cdf43abbedfc`

```dockerfile
```

-	Layers:
	-	`sha256:a186141eb29ae766b50e2023b56260f9a4bfeed9e0a6a4884993fc75567eaca6`  
		Last Modified: Tue, 13 Jan 2026 07:38:41 GMT  
		Size: 7.5 MB (7495613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bd84439e93a29ee7d24510258bd76bef38ec1405f1168beaa93ea5b72812908`  
		Last Modified: Tue, 13 Jan 2026 07:38:42 GMT  
		Size: 14.3 KB (14303 bytes)  
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
