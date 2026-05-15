## `clojure:temurin-11-bullseye`

```console
$ docker pull clojure@sha256:6946c5bfa074cf0fc49aab7282513e6cb9cf99575861f08806adc324d29f639b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:58f9e0ca75835e79790e6bc2f640c7ff5a152a79759af3576cb788df24bc1ffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269274281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4da8526e0aa4b103e9c9a388d605b30eb0ca0131632c9dd848f5453bf5893f2`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Thu, 14 May 2026 23:34:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:34:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:34:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:34:26 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:34:26 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:34:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:34:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:34:40 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bbe7a1cd518455ae090fbc7a773c0ab830777bdb0eb1f247b1c5d24a3c91af`  
		Last Modified: Thu, 14 May 2026 23:35:02 GMT  
		Size: 145.9 MB (145886262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a6f690ea5319c88cd9dcb13b42d7f57c8213927459281b616e2762156da0b6`  
		Last Modified: Thu, 14 May 2026 23:35:01 GMT  
		Size: 69.6 MB (69624028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64882596d14d950b5ba150cfd0dcf5d9e6e5d606b02449ebb884b609a550a926`  
		Last Modified: Thu, 14 May 2026 23:34:58 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:16c5e74b1b500068c964d4260a563bef18d7beb062f796981b9eb1e018eaa532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7442157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68fb6dc10623829afaff7178dc4c89537e239d49a6f7a2283617e03dc727346e`

```dockerfile
```

-	Layers:
	-	`sha256:cd3f2d5aede3e692a1fd887e3b7e335ca3f0495408ab7b9029fa74b78b4e166e`  
		Last Modified: Thu, 14 May 2026 23:34:58 GMT  
		Size: 7.4 MB (7427794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6cef1ef78c32c2904373190c4a50fffad7cde5ba183f1f521d728de4c179bee`  
		Last Modified: Thu, 14 May 2026 23:34:58 GMT  
		Size: 14.4 KB (14363 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d53100c535fdd6e99d83ba61e0200e350c1eec9880d4f51d7d9be05280d54dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.6 MB (264600150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42ccb22744724384795aa577c4b428b3dea0526de9e1e82691db91517d66482`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Thu, 14 May 2026 23:34:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:34:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:34:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:34:20 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:34:20 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:34:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:34:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:34:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8bf2c09bbad533bbc490d112b59439f90006ce0c83a7b1e435668fc06a5fb3`  
		Last Modified: Thu, 14 May 2026 23:34:52 GMT  
		Size: 142.6 MB (142582199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e767a19cf8c17a611763574df2085a0b1a7745f257655d1c923b275e1b8a08b9`  
		Last Modified: Thu, 14 May 2026 23:34:56 GMT  
		Size: 69.8 MB (69764094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d2eb42b1a0035311078c8d2dd5429e282741f8d9e46465e4968f99b95ab549`  
		Last Modified: Thu, 14 May 2026 23:34:52 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:bce4d3f63542a411987647c1697916bbd8767956592b718ac3fba30caad712a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7447992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdd9381d0718f774340bef1c8923f68859e6c116f7c8df9a6b79f473d8441d06`

```dockerfile
```

-	Layers:
	-	`sha256:7583c498acef2340741f862adc1939b63e764d0e2808d57c01937361592864dc`  
		Last Modified: Thu, 14 May 2026 23:34:53 GMT  
		Size: 7.4 MB (7433511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8de162db2671d3c3cfba71e44e44aaa81ae0ab176b28d78e467ee9097ef49a34`  
		Last Modified: Thu, 14 May 2026 23:34:52 GMT  
		Size: 14.5 KB (14481 bytes)  
		MIME: application/vnd.in-toto+json
