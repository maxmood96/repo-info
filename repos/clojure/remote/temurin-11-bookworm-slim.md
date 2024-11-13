## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:558835120b086a6dd38750c4e1397834b657acc8f463e9b14cd8ea9af5217776
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a498bfb78e2c727b04873087d07a43c4cc9df1effd7f750c0e0c0bc22daf730e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244217074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db34f630e43a71edaa8ea5b43f8289fe33ecef0c9e5ec99077de45945ed365b8`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16924935036548fa95a02683aa5d1add89142f550af9728b746c4590c02a3b11`  
		Last Modified: Tue, 12 Nov 2024 02:23:43 GMT  
		Size: 145.6 MB (145601329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6d715b25524740f3f263d2cd12eb21e9052a2e71d8473cfbd29442a26abe16`  
		Last Modified: Tue, 12 Nov 2024 02:23:42 GMT  
		Size: 69.5 MB (69487107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f932dc65acad4e43ba9e8b67dd6f93713891b99c55d107f965afdb6e7880f9b`  
		Last Modified: Tue, 12 Nov 2024 02:23:41 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f791e11ab4e67a03f1d7f9e08fefe752242ae79a4a4677240858a91cf5a773d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4955109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c508220ca6ecb38b7bf84d6d3cee6f7e36174a0c6b8bb7d2ceb913c7e27b23e6`

```dockerfile
```

-	Layers:
	-	`sha256:13b40adddb809205d1a9719841334d24ae84df7d1991624ea4c03fcf5a95ed0a`  
		Last Modified: Tue, 12 Nov 2024 02:23:41 GMT  
		Size: 4.9 MB (4940799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a446804ead9ebbb785b9446d7dd9b00cd1e4dfa4b21baacf8556fe844729959`  
		Last Modified: Tue, 12 Nov 2024 02:23:41 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:414e725d2f61a594ef3f4bed3e94cdbdb30a4c738f21af29493c3c53e129358b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240881806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63f71ab8814ad9fc0fe6bd2227fa0183a5abf45db737bb8654cbe15244a4c55a`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82eafc01c21661a2065d8f4e95f0d9c0cfc8e2a654df347633121c6a0bbeb6e9`  
		Last Modified: Wed, 13 Nov 2024 01:10:37 GMT  
		Size: 142.4 MB (142389107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e834418adfce1503828e21b5a3043a3e920a8cfa65933e979001745a683d5c8`  
		Last Modified: Wed, 13 Nov 2024 01:14:26 GMT  
		Size: 69.3 MB (69334699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ab83f86a75de5fac00b0fbefef60054b46aa665d562418ab3bb793ca7e8ce6`  
		Last Modified: Wed, 13 Nov 2024 01:14:22 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5355ca193b87fdb25ec614aa22bc7a9929d30c6bb05acba2ae27cc1a4eec594a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4961611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739af3cfb8ac9e82c1a75d1a34441a7304d250a931314f6d8e0827b5de23c225`

```dockerfile
```

-	Layers:
	-	`sha256:aed5542e740457dc6443343e40151afa997379ed2258d99ecba224769cd8210a`  
		Last Modified: Wed, 13 Nov 2024 01:14:22 GMT  
		Size: 4.9 MB (4947184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2118cc26abb2ea53298119d009d0ae448daa4da4c0d21a20e9236845ea01788`  
		Last Modified: Wed, 13 Nov 2024 01:14:22 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json
