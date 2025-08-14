## `clojure:temurin-11-trixie-slim`

```console
$ docker pull clojure@sha256:3df8b78804a61a0a959fdf5d0d78e7f11610b9a554b2eed1b6ac3218c15fa3dc
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

### `clojure:temurin-11-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b3a3cf6019cf01bf92887a561a54eaf9bc46658c5ed9bbfa382bc181ec9bc3c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.3 MB (247272543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ed428de99622a8c04b9333751c63cf9c016f55a0ecb2c17235697ebebf2a14`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b8687b87eee44f41409cbb2b10b3cbb6c4547e6b1289f9a6fbf96bb64686c2`  
		Last Modified: Thu, 14 Aug 2025 02:36:52 GMT  
		Size: 145.7 MB (145658173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c742a96288c7cd7598feadc20d43a759afeeed52fe81670d729e2e2cc5c112d`  
		Last Modified: Tue, 12 Aug 2025 21:36:15 GMT  
		Size: 71.8 MB (71840441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ccfcf029fad84b4a308055e70da930c87c18624faeb88d78c0140c9279a1fa`  
		Last Modified: Tue, 12 Aug 2025 21:36:10 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1491ebb96819ec8747a6a81afc844256d18f1f147b64e0cd1b383c531bc4c622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:440b0362d062d370b0f1ff2f9eeeb1935504f167636c68d10be5ddb4eb845ad0`

```dockerfile
```

-	Layers:
	-	`sha256:764b0c4f753566a5d6edf070a548785b96a8823d56876b627d58b605153ef809`  
		Last Modified: Wed, 13 Aug 2025 00:36:24 GMT  
		Size: 5.3 MB (5275349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62026e88314a8a3c436a2e5341d37c3b1237bba2a8bf9d4c722854a22aa6e1ed`  
		Last Modified: Wed, 13 Aug 2025 00:36:24 GMT  
		Size: 14.3 KB (14286 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:39ce449ffb81b2d1e8e7485b8bd9effb206a03a9266bcd5d08b0a129e9ff7a83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.3 MB (244260726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0dfc679e258e6c7d4807dbeb0ec64db53f6eff4ae53423060e2f1e9c8475651`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2395918234ca23c280293c9b6bb19a201034a33109dbbf0afa5c7779a29f14a5`  
		Last Modified: Thu, 14 Aug 2025 17:44:43 GMT  
		Size: 142.5 MB (142460542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ee8e3d7a43371011fb2c3b4207b3237aec0c8010e4de615d67a496b6ccfe78`  
		Last Modified: Thu, 14 Aug 2025 17:44:53 GMT  
		Size: 71.7 MB (71663496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4bb08664c8920d61056f1e123d7cd10a27abdb13b77cf0dee9416c9bbaf84e`  
		Last Modified: Thu, 14 Aug 2025 10:23:50 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1cbf3934f3db3d09b523e84228c842d48c85e2812a4332efd28b038f662ac206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5296139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a2199b7b534fcc1a8bf2340b5b193737837ee2d5761cbac1ed6f6e1d6254fe`

```dockerfile
```

-	Layers:
	-	`sha256:193b7cd347c18afc6aa3226f6613e17a32ffe733e8d0c6399ecb3ae89164a7f1`  
		Last Modified: Wed, 13 Aug 2025 15:36:34 GMT  
		Size: 5.3 MB (5281736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61a5670183ed85e6b642f251a339a49c93a08f5fbc20543c36f805e40ed6a0ed`  
		Last Modified: Wed, 13 Aug 2025 15:36:35 GMT  
		Size: 14.4 KB (14403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:73d709fb9d14f86a181fab31a277dc16798600a096f9d09bdbc6d05b75da367b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243694500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6305d251f2c29ed5566ea7e4ae93b6df4df3ecbc858ca8c2e48981c7a4dd8c15`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6e774626a37cdf4a89f92b71735aff9710b08e3d1ccf38f51ad2b342685be8`  
		Last Modified: Wed, 13 Aug 2025 19:37:46 GMT  
		Size: 132.9 MB (132853313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e8ce859e1fb67abac0d2dbda67eabac1c17aa3f68815b69fc9519dcaf10e21`  
		Last Modified: Wed, 13 Aug 2025 19:44:47 GMT  
		Size: 77.2 MB (77246328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40da8806e7a3728632481114e21bf1575b591c10a8dd0910c733a2ca071e07aa`  
		Last Modified: Wed, 13 Aug 2025 20:27:04 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5256c64cd5a350a2a7684939862eac2b0ff7dcc8d3f9693e206eaea2a951dfc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5293438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42be9b6c437a03a500c2c905c9997d7dd2031acc51dc538ef983adfdec22526`

```dockerfile
```

-	Layers:
	-	`sha256:983adb5eeef15b9829b888565929aa44d3c3d066457e1403eec247115c7f2a31`  
		Last Modified: Wed, 13 Aug 2025 21:36:07 GMT  
		Size: 5.3 MB (5279105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:661cc3bcaa1add685ab99949bc4eb601fadb00f9c4eeb8db17465e79dffd0881`  
		Last Modified: Wed, 13 Aug 2025 21:36:08 GMT  
		Size: 14.3 KB (14333 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:28595e77d05acc5e670fdaac4ff1e870559017e3bc50c150bc467d6384b59a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228260327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1eb74af0215277bf2c82cd99dbe81bdde36d8902c3534ee73a47489fc49c27c`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3afd6b90bbbac2c87c011fd5aabaebc7a8db7c364da32e28cd66feb8c4739e32`  
		Last Modified: Wed, 13 Aug 2025 07:06:59 GMT  
		Size: 125.6 MB (125622113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5859278850034e0ab94e0a101d614ccbcab508e5af2b0a3b80f9675563cdc56b`  
		Last Modified: Wed, 13 Aug 2025 07:11:07 GMT  
		Size: 72.8 MB (72804512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66bfb7d000ffe65913eb13074be1d680deec929a65c5437989c40e85813d3f57`  
		Last Modified: Wed, 13 Aug 2025 07:11:03 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8747bd4cf22484a284e3359fd4fae135f64e0579d0d84d2c99b6b6ef9977eaa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5285563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d323808d132d19abcc75b5c8ba83a17cefac9e0e59be52c1d1a23e506de684c`

```dockerfile
```

-	Layers:
	-	`sha256:17ab9135bed8a140ed321022b31dc6994f1b4709d6b9a71ac76eb7e926997438`  
		Last Modified: Wed, 13 Aug 2025 09:35:50 GMT  
		Size: 5.3 MB (5271277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34b3e05b64523fa2d962005dc14501f4a3daf25a13343702508a7549c0705b87`  
		Last Modified: Wed, 13 Aug 2025 09:35:51 GMT  
		Size: 14.3 KB (14286 bytes)  
		MIME: application/vnd.in-toto+json
