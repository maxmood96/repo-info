## `clojure:temurin-26-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:81559f4a1e87e1f7e07487eb69ff94366d6ea16febd444dd9a419ab54d9ad016
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0a6cfcb83d48805398945ac826e6e071a44349e0ac757f2c13f28d1dc78e3264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.9 MB (183898370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a4c6e3cad6348d250691aabb52c1d315fa8f0afcde3949e69475012254386b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Thu, 09 Apr 2026 23:37:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Apr 2026 23:37:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 09 Apr 2026 23:37:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Apr 2026 23:37:16 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 09 Apr 2026 23:37:17 GMT
WORKDIR /tmp
# Thu, 09 Apr 2026 23:37:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 09 Apr 2026 23:37:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 09 Apr 2026 23:37:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 09 Apr 2026 23:37:30 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 09 Apr 2026 23:37:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbfb952fdf329199ea9fc994a44ab608997ecc88c7cb30ebe91108be655f822`  
		Last Modified: Thu, 09 Apr 2026 23:37:52 GMT  
		Size: 94.5 MB (94455693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6360dabde100c52ba1402038b68cfb8e1a510b0f53d639343aeda3152632c2cf`  
		Last Modified: Thu, 09 Apr 2026 23:37:51 GMT  
		Size: 59.2 MB (59183618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1825246625ee77a71d0c51ff7a4f11dadea62c07af96ec6359083501d0d4fe`  
		Last Modified: Thu, 09 Apr 2026 23:37:48 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecddabb37a77ce031529d87072e97e55c7a6cadfd9188fae7595b8f0c7ec0a47`  
		Last Modified: Thu, 09 Apr 2026 23:37:48 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:197c82b4de9064f736f294c522ee45f7b7e5d51b5cf8c743fa0c82201633067f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5301386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc5a3bbf4bb1c6121a51efffc39d029c1a8c097b668b1b53aefe90d97a8f55f`

```dockerfile
```

-	Layers:
	-	`sha256:aa2a68f3a0b51879191fc5dcbb1b4c2ed577ba3c807d9ecab9e3ee0fdfb1c77d`  
		Last Modified: Thu, 09 Apr 2026 23:37:48 GMT  
		Size: 5.3 MB (5285557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a217a9c785729786433e897205302a00bf074c07efcb8c29e9ec8675bbd4204`  
		Last Modified: Thu, 09 Apr 2026 23:37:48 GMT  
		Size: 15.8 KB (15829 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ee7ce19bc7e2fe32bae55a5ce2d40afb68c06e1fa7d1a770c9b159ebfa9906e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181464498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb20201089457f8f52bc4a998995faf893f0f25f4b332f88b5cd1e3b36ceca18`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Thu, 09 Apr 2026 23:36:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Apr 2026 23:36:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 09 Apr 2026 23:36:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Apr 2026 23:36:57 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 09 Apr 2026 23:36:57 GMT
WORKDIR /tmp
# Thu, 09 Apr 2026 23:37:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 09 Apr 2026 23:37:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 09 Apr 2026 23:37:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 09 Apr 2026 23:37:11 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 09 Apr 2026 23:37:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304ed5daff846a315d34d00fc32b6f16442e7a86a659d99e6f30cd239d826be2`  
		Last Modified: Thu, 09 Apr 2026 23:37:32 GMT  
		Size: 93.4 MB (93395181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49ca0ac9767187ad412aa67e04504363a83ede463f99bfc96d83c4d3866fbe3`  
		Last Modified: Thu, 09 Apr 2026 23:37:31 GMT  
		Size: 59.3 MB (59323585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9628a7b79aefd758c6edd23182ebaea040127201504cf7098a6f6faa7333a86`  
		Last Modified: Thu, 09 Apr 2026 23:37:29 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206a972cdc99d660458e53393d03ea1e6421a3530e97f0888e9e13fdd3ed5f78`  
		Last Modified: Thu, 09 Apr 2026 23:37:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6d6985a790891c8c43272eaa0de2429d7140c96dd834e5016242c855d2b60a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5307233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b51a0f9f858739a56f314cd4a6fe47091410a4a4c5a109f7a30f4af1c7e47e6d`

```dockerfile
```

-	Layers:
	-	`sha256:81a6c57f7b7ebefb1f34fb3ba2089abcd6ffbf7fb4024264898205de06563453`  
		Last Modified: Thu, 09 Apr 2026 23:37:29 GMT  
		Size: 5.3 MB (5291286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab00d51ac47e58ee05a5d0d561fa14d4140a3c6b692ae4ed6548e95978b87b9b`  
		Last Modified: Thu, 09 Apr 2026 23:37:29 GMT  
		Size: 15.9 KB (15947 bytes)  
		MIME: application/vnd.in-toto+json
