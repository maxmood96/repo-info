## `clojure:temurin-11-tools-deps-1.12.4.1582-bullseye`

```console
$ docker pull clojure@sha256:216187e2e83413c6395ae1474bf1982a535472dc050e6827fa73fc3d0a5256bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.4.1582-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:82260228fbaebaf643ea24d357818f997a6e86ea820ca4f529f65da217e11270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.3 MB (268280434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:533460aad04c42feda1c6e53c135ad5ba4c07868e6a58f8736fd15a7ab15808e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Thu, 11 Dec 2025 22:38:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:38:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:38:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:38:32 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:38:32 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:38:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:38:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:38:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:437b5b60e3a4b64e2c621589a67483eeef6d4b3fc4926655006ef41bd44f71dd`  
		Last Modified: Mon, 08 Dec 2025 22:16:49 GMT  
		Size: 53.8 MB (53756413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ad81e69e2879af0dbb56abc75ccc83c5263d62041bb6b2fe1d4faad09c7570`  
		Last Modified: Thu, 11 Dec 2025 22:39:09 GMT  
		Size: 145.0 MB (144966652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888daadf09cee0a23a7b8cc4d32e11526271fa3310021cda44917e780ca60cff`  
		Last Modified: Thu, 11 Dec 2025 22:39:19 GMT  
		Size: 69.6 MB (69556725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86222cc15d3a5e0d01e4cff1904bc7b569bc58dbc370f6d6fb696de3f7431a0`  
		Last Modified: Thu, 11 Dec 2025 22:39:12 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1582-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:255cb372875715cd3a93d85ca94a78ade43e301b033c3f69cedfbccfa3146f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f84b23bb3e386a24d038ff023bb4fcd8e3eae809b5384356f6691e13887e85f`

```dockerfile
```

-	Layers:
	-	`sha256:254772bdbb055f3dd7308058e2c721e22bb2e6b7204e529e0b2aa788cf300d97`  
		Last Modified: Fri, 12 Dec 2025 01:35:21 GMT  
		Size: 7.4 MB (7415808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a706436350255fc4a1f6af68a87a3697a37c11916f525b7a4f00a26a6a631859`  
		Last Modified: Fri, 12 Dec 2025 01:35:22 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1582-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a5061976f0527939c2f66b32d80be5e69c5af31c0ddc600664da5f062ea9b8e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263676974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ee6efbc5495f0c47c42ef7ef8be5f3dd643e2891e0ef060cf748be17d0eec67`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Thu, 11 Dec 2025 22:38:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:38:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:38:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:38:19 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:38:19 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:38:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:38:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:38:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:24bca79f74a34f86894c8fcdc6ce8d7dc3c11dd0c76b7e9fa80c7c64df65d166`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 52.3 MB (52257713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a736d8eff0febdaa6230e690cd033040c11a6271a2bc61ce0775cebbccd4143`  
		Last Modified: Thu, 11 Dec 2025 22:39:15 GMT  
		Size: 141.7 MB (141731574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da78ff0814aea74aa5d3feef3aa29d8c837aaf5a8a85fa875ce495e6b3257b5e`  
		Last Modified: Thu, 11 Dec 2025 22:39:09 GMT  
		Size: 69.7 MB (69687044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee579c98243d9761c6addc7da543aba07f9770206ace759e6e9f61f7a7d8a22`  
		Last Modified: Thu, 11 Dec 2025 22:39:03 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1582-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c9ad4650461dd22d520cc7affd82c5a4b34635df7245e60ac37b1f4b2ce5ee4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a14234cf2e0a8ba9bc78fb1edb8be4f22fc03ecd5aa2223f45145a49b5065f8`

```dockerfile
```

-	Layers:
	-	`sha256:f95c275bd62d9ef1ffe241344d81d5ff6c91e992f795cd9f364a71dc15b94962`  
		Last Modified: Fri, 12 Dec 2025 01:35:29 GMT  
		Size: 7.4 MB (7421525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:504248ab8350bb6e4777aedd20392053c0df667f017859d164206fcd7030f2a6`  
		Last Modified: Fri, 12 Dec 2025 01:35:30 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json
