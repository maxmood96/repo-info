## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:82ef893f738507bd9dbdae64c4381aee602d3132bbde55386e7c9febd5096a1e
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
$ docker pull clojure@sha256:5c319d8294ebf5b875d0a9bbb9f1a2d019b7e193933dda9cb035472e36d504ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150074639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf6e886551444163d5efe5623df5bf866e8c1e147717f70d09a0a334f2fbce9`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:40:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:40:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:40:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:40:20 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:40:20 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:40:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:40:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:40:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34b83dbd5549e7df6c098e2c1c5a1316dcb4f88afc4ae6eaffda6de2ca91f65`  
		Last Modified: Thu, 04 Jun 2026 17:40:54 GMT  
		Size: 55.2 MB (55198725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf0a4b2c7063925cf1b716ccd3ac49e73b35a77742f5bdfed81b200865d8da3`  
		Last Modified: Thu, 04 Jun 2026 17:40:54 GMT  
		Size: 66.6 MB (66641728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41eaf199b0767da60385cbfa388be250519f0c072d681024ae7e7ea64ee98e8d`  
		Last Modified: Thu, 04 Jun 2026 17:40:51 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:43cc8921dac8228705e9b0e8ae69ae7943cb8faefa394e20be1697cddb5f03c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5248743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e08b5df6ae180a1c0636301eab5d26c6d4a54718ef32d3552dc010ddf7abca95`

```dockerfile
```

-	Layers:
	-	`sha256:65385da24bd8194b9ec4c51097c3cd6102b35932099e16934c96a7f7b4299d0d`  
		Last Modified: Thu, 04 Jun 2026 17:40:51 GMT  
		Size: 5.2 MB (5234341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bdb98ad48359fd1f8f034e1c9d1a1706b5508adb0b63d4d1a885c21cd89b594`  
		Last Modified: Thu, 04 Jun 2026 17:40:51 GMT  
		Size: 14.4 KB (14402 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:aa2904aa7f7be60d2134bfb48ca206a77466d9e13aff467005f89c26b3de6c98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (149031948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69221793a4499d57d55a9dfe916ab8fdafca667dedbd9ea9081c32736d7c52d9`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:40:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:40:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:40:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:40:38 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:40:38 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:40:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:40:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:40:53 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66a8cdb9b996ccfa6cbc682f502b62c6ac719764d289ab86c46aa25c2729277`  
		Last Modified: Thu, 04 Jun 2026 17:41:10 GMT  
		Size: 54.3 MB (54272936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eaad04f9d144652056419df7f40824a41e1677901511ba204da36ef11a828ce`  
		Last Modified: Thu, 04 Jun 2026 17:41:10 GMT  
		Size: 66.6 MB (66643325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168dc3b7e5fc3abe9c0345dd00e20cd720c58adb216a4864f6090f7f7e095dbe`  
		Last Modified: Thu, 04 Jun 2026 17:41:07 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:af6cbc1ec6613e5fc7fdd8d312ab9c68dd51d1b6e565090ae07f2796fb6b3149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a2141860cb895ed6b62a2f92ce9f827451d38b511cef8bb7791544780a27fe`

```dockerfile
```

-	Layers:
	-	`sha256:fc1dfad9406adfeedce6470e892ee3321d440f5d6f80b0279e0a6c1ef66d5304`  
		Last Modified: Thu, 04 Jun 2026 17:41:08 GMT  
		Size: 5.2 MB (5240802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f281f2ad8a53cd06452ca59fc96069e10699430d796e8fa99cf88b9f764c9def`  
		Last Modified: Thu, 04 Jun 2026 17:41:07 GMT  
		Size: 14.5 KB (14520 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:7cbc7b5195853cfd973a5f73a1cab979a92dd38032ab6d54f94243860fe9caab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157221399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196c44825991fb875dae3d03d80d3b703b0d19c6c8a7d7d6a88b34192405b769`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:42:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:42:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:42:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:42:27 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:42:28 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:43:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:43:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:43:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:562cecbb5aa529d280e58ef1f95f14cdcd37a90c5ea9181798a78377e934e6e7`  
		Last Modified: Tue, 19 May 2026 22:35:14 GMT  
		Size: 32.1 MB (32075742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d768c11af83dc4578c7a5c5709036ab2ff60f6f82797e4be610d62ea048f44c1`  
		Last Modified: Thu, 04 Jun 2026 17:43:57 GMT  
		Size: 52.7 MB (52669122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f455ead53eed8cac3e8286c09397d374ff4525ffd8ff0ce176318ca514119971`  
		Last Modified: Thu, 04 Jun 2026 17:43:58 GMT  
		Size: 72.5 MB (72475889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4528a9e327610e019ff01b5ca316f32d6e293054176cfdbf8b931c1630abfc0`  
		Last Modified: Thu, 04 Jun 2026 17:43:54 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a466c4e6d83caa748f2e2f513f74de5565bcf19a75d73e2ff059321b64b5e2a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5254544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e9ce77a8bad9d72875cf17280f781cd7dbc1c859594782140a926a7e6b1989e`

```dockerfile
```

-	Layers:
	-	`sha256:9b75fff9590c2c0c17fd68a4dca7a72ea4407e2fa5e949b738bf700476682a1a`  
		Last Modified: Thu, 04 Jun 2026 17:43:55 GMT  
		Size: 5.2 MB (5240094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7bc479de547c85cfa394f0db5d56c1febe7c2080c3b9e0bb889ec11cd6e997a`  
		Last Modified: Thu, 04 Jun 2026 17:43:54 GMT  
		Size: 14.4 KB (14450 bytes)  
		MIME: application/vnd.in-toto+json
