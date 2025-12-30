## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:01a4903b5e1d978cf231f0b3aba09769457a017f5fc34ec7e7835f77804ba7f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:27a11aaa5398fd3106a4b5302dc91cd374893c141822b17b9adc3e1dce172ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152639491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f50bb334b8fbc76fb804f54aef296d50801cf597d08b7f4a5cf0f985a30b4b84`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:51:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:51:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:51:06 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 00:51:06 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:51:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 00:51:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 00:51:21 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c849172ea6a19bd4c8c93920c4a8bc7300ba8a00c06dabd33724b8b93621a22a`  
		Last Modified: Tue, 30 Dec 2025 00:51:59 GMT  
		Size: 54.7 MB (54733390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585f01ecd5e836ca871821ef4864b557b26a6257bae8d94ad496024006364dd2`  
		Last Modified: Tue, 30 Dec 2025 00:51:50 GMT  
		Size: 69.7 MB (69677034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc40b9f25237d532a52e460aff02be3426dc118f9b5ee14bc976f2e289f7484`  
		Last Modified: Tue, 30 Dec 2025 00:51:46 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4d453397df5e8e9ae8b9a07ede84e264a9065ed6fd5f48054b9f6650933168a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:178ab58560a4dae24ac6f2a419930bc236a329004e6a7975c3abc4096e31adeb`

```dockerfile
```

-	Layers:
	-	`sha256:519ae8694fad23981825e21ad6ef3f72f6de5e5bc0145da3d21b92272e3fc409`  
		Last Modified: Tue, 30 Dec 2025 04:48:22 GMT  
		Size: 5.2 MB (5234998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e22ad6b6e28f26e7b2e32ee680055299f91883ffe2081e882ddcfdd3215eceb`  
		Last Modified: Tue, 30 Dec 2025 04:48:23 GMT  
		Size: 14.2 KB (14247 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ef744e6e7a17a25c51700b906c10c951a0675771a7ff026c8f36c27fba4ba0f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151476247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bef68d966a5060957c65936eafe2c3199eb7ce928c284641e75210c0db575669`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:54:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:54:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:54:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:54:39 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 00:54:39 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:54:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 00:54:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 00:54:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30214f1492318f4a2362ac906f8fa13aa70826716091930a643fa5f3a1629d1f`  
		Last Modified: Tue, 30 Dec 2025 00:55:23 GMT  
		Size: 53.8 MB (53814985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfd625757204cbcf3b8ee9860859b49d5ae6dd1a2ee4926f751f1847206c5f2`  
		Last Modified: Tue, 30 Dec 2025 00:55:24 GMT  
		Size: 69.6 MB (69558408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7c33f6110b21403eb225f70a5d8fbe01deddd622f03641cc4d6b4b07cab97a`  
		Last Modified: Tue, 30 Dec 2025 00:55:17 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:af12e6cece6008e8b40d624111468a53fe687b979c7ed89e6501f4fe8dc645ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff944d3254cf30a7fda1c30f85aaa8cb97cb6342962149587ede4ab755e40fd`

```dockerfile
```

-	Layers:
	-	`sha256:35f4905d9430b2ba2ee6181348d785405c7e27c9124f5cfb3168b40feb587853`  
		Last Modified: Tue, 30 Dec 2025 04:48:28 GMT  
		Size: 5.2 MB (5241457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:867926429341e867a4dd615c276754346c6a191c871671a0391a858fc993284e`  
		Last Modified: Tue, 30 Dec 2025 04:48:32 GMT  
		Size: 14.4 KB (14366 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:81ab98aa6b2e258b6efb40f43b4ee46d052525ab09db740b3634cb9e25b6354a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159754592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44ddb909c6b1cad44f94ddb9c0ad09fee88cd1c824047a62b36281e5542f69ac`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 05:10:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 05:10:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 05:10:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 05:10:59 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 05:10:59 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 05:13:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 05:13:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 05:13:17 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b7648f01f6858fc79caf032b4b9ed2f7e43e57f4621dc8cb36e84eb86399065b`  
		Last Modified: Tue, 30 Dec 2025 01:48:36 GMT  
		Size: 32.1 MB (32068844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294a0af0a5f1d7909ae6111a947cb6482d2e009c862439fa97b16a3ed543effa`  
		Last Modified: Tue, 30 Dec 2025 05:12:19 GMT  
		Size: 52.2 MB (52175137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9e994ae4c54efc5fd7ff08bd05f0c7ccdf1d11f64f5dba424451b96c4121c7`  
		Last Modified: Tue, 30 Dec 2025 05:14:18 GMT  
		Size: 75.5 MB (75509965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fccc00731b3ec0da0e8461afe1df7db4940edbad3983881625c343ccc2541a3`  
		Last Modified: Tue, 30 Dec 2025 05:14:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:46b54f75730e732458f2972a92029100e90d7b042bb37b070be3eb5b3b68db9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c5a2a29dfc0354b4b8d30f7620146331929dd66368a3ad16317940a5cb329a`

```dockerfile
```

-	Layers:
	-	`sha256:50d0a11da743614ee6305d9106e978d87e8592c05e6a514de27c54c7bd0f92cf`  
		Last Modified: Tue, 30 Dec 2025 07:39:34 GMT  
		Size: 5.2 MB (5240749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32b992434a947f73702baba35072bd123ee9bd575975f20aebcc46e5ee367769`  
		Last Modified: Tue, 30 Dec 2025 07:39:35 GMT  
		Size: 14.3 KB (14296 bytes)  
		MIME: application/vnd.in-toto+json
