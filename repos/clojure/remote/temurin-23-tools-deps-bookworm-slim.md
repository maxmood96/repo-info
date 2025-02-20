## `clojure:temurin-23-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:2e4d1a22923bab97633fb247618d4d5e2ff0b85573a4c4ee3579157a773eca44
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5cf77c3a71c2780a726b5eca4e5934cffd6bf4ea963e97b34b098bdb438fedba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263059810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc192f9f3a115f7eb629d2f7d7d019441a8ed68c5cd76a391c9846b8ce97445`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 04:27:59 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04bde6b35577714d67e59601cb29a34de8a40b02bddef87d4a4ab967e9c84255`  
		Last Modified: Thu, 20 Feb 2025 02:31:37 GMT  
		Size: 165.3 MB (165316243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c32a3dce638e9eef7f5dd2338d0f92eb40e7a4690cdfdcb5d6620a059cdb55`  
		Last Modified: Thu, 20 Feb 2025 02:31:35 GMT  
		Size: 69.5 MB (69530224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca33e7d023d08671f1d407eb54e16acb50e106a43bf23c0aa2fa85fc9f2489c`  
		Last Modified: Thu, 20 Feb 2025 02:31:32 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe765e9985b8be7a39eef9ebbd47021eecda70a3088a48d1d9ac3125c2e5b1f`  
		Last Modified: Thu, 20 Feb 2025 02:31:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:09487cf41572c5f95cc3158a77d2f2f38c275a00a5f659bf1018d2e6234a5a1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4933450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:044f09182387c574bb1e57682d30c7560d249b7435cf9ff7da77575739c7c8e7`

```dockerfile
```

-	Layers:
	-	`sha256:36f046eed9cb0bea449f644a8e57fafdaeb9aa613b8933c8886e3f14d862e822`  
		Last Modified: Thu, 20 Feb 2025 04:37:52 GMT  
		Size: 4.9 MB (4917572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7388d35e14d7271e0e235769880ce371a6a4ca43745f00bd9d8cec374779d555`  
		Last Modified: Thu, 20 Feb 2025 04:37:52 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1fb052d7151718bae852dbad3f50f115bf5e4f2fb018030ba9108c5966fd7247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.8 MB (260762597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472a1974848cddead05fc7cb42d8510e5583d95748dbeb8eac207af95fed9fbd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 04:29:51 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d3d2b1c1dfa2977b74e155013c02da80d2fb8bfea30462dc1a42ab04348739`  
		Last Modified: Fri, 07 Feb 2025 06:56:04 GMT  
		Size: 163.3 MB (163341435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a164074736d81268f8e5e171b395f6f8b70f0baa13129dc5d8a819b623abd43`  
		Last Modified: Thu, 20 Feb 2025 04:01:55 GMT  
		Size: 69.4 MB (69379239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff9ac6c61ff9930b0faf771fc7991906feaaf16faa81c2898cb9510210fba67`  
		Last Modified: Thu, 20 Feb 2025 04:01:45 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db928b52e49e2256f7a7cc26b9557ad86a5446d050f6dc972a4eb4a9584d593a`  
		Last Modified: Thu, 20 Feb 2025 04:01:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3579da6bd4e1d60a257e8a3f2cb4010de665e93934223528d2f26984f927fc66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4938708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da2332ced035ea2ebbcb70b2e9e04c8ac7dc25a2659b99c5e39dc23728253e5`

```dockerfile
```

-	Layers:
	-	`sha256:cb051926f5c3559ab85998928ec67ccb0f4329ca906210d067cdf591cbaa7c03`  
		Last Modified: Thu, 20 Feb 2025 04:37:55 GMT  
		Size: 4.9 MB (4922712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4305ded861fa7ad4823eab14cfd8c39b0a0d535b537142b245c9800f0de28ff`  
		Last Modified: Thu, 20 Feb 2025 04:37:55 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
