## `clojure:temurin-26-tools-deps-1.12.4.1618-bullseye-slim`

```console
$ docker pull clojure@sha256:276d683971a3d400dcaf0d2216674bce883ededb2c3061815c9a44e0d812faf3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-tools-deps-1.12.4.1618-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:559f2615f9bafddef889d4c186da6567682ee2db88792802e9fae703208f1931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.9 MB (183901051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9901e1db9d42238bfda248af0136d672c80bd1a0f59ca0dedaafd75a55dc84`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:22:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:22:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:22:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:22:12 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:22:12 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:22:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:22:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:22:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:22:25 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:22:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7263c37a27b96bd5e0c0de77a44122fc986156c49e3c82b0ba12448611753e10`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 30.3 MB (30257934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39c6a3f5f8c7c324687421581c53b628cf7335e3668e0a73517a7b226ea30b6`  
		Last Modified: Wed, 22 Apr 2026 02:22:46 GMT  
		Size: 94.5 MB (94455697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a04f92328f4bf05bff248b1bbb7f764356c1cefefd8ad2abac0db77de78801`  
		Last Modified: Wed, 22 Apr 2026 02:22:45 GMT  
		Size: 59.2 MB (59186380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb209f93096d8330a616b21b2991443cf2934edb7c6d0c12dd81a67c96ecef83`  
		Last Modified: Wed, 22 Apr 2026 02:22:42 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8602692e2a6877e4378223632137d762528e5c712b802f7a58a020983d1a4702`  
		Last Modified: Wed, 22 Apr 2026 02:22:42 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a2eb99f86614d1e528b080df27423fa7653e8452705b0b2215b10dc41e2f4ef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5301386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547ef0eb8b494fb3d4b96f5649588e5c12262ce26fc90b17f5def94c9f1a89b1`

```dockerfile
```

-	Layers:
	-	`sha256:a583c4dee4c196b0630fdedd3a7757adf783fc4972d2618daccff7c542d7201a`  
		Last Modified: Wed, 22 Apr 2026 02:22:43 GMT  
		Size: 5.3 MB (5285557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae04a1deaf0e92233664006d8f1f50959d3d2d1f56565be55822b3f197c0adc2`  
		Last Modified: Wed, 22 Apr 2026 02:22:42 GMT  
		Size: 15.8 KB (15829 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.4.1618-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4430446c87aab473e96f251707b82e573d22472813d3895bf4fca0436cb0c8d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181469775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b39b947192990f94ad83d4816c40b49bc9419ef22b790431fd57bd23c8805f4d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:25:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:25:09 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:25:09 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:25:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:25:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:25:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:25:23 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:25:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56be05e18c5d9b4cc9a6a882fa03b8a740d9362f4266f03e250245a28a24ec59`  
		Last Modified: Wed, 22 Apr 2026 02:25:44 GMT  
		Size: 93.4 MB (93395213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ac629b76de29b8a71cd9853b0b9e97c1752bd1cab6016aed4bb95f524b41bb`  
		Last Modified: Wed, 22 Apr 2026 02:25:43 GMT  
		Size: 59.3 MB (59331009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57cc9202c09facb2ade382c8378d011467bb98dfe42c45b713998939261c0348`  
		Last Modified: Wed, 22 Apr 2026 02:25:41 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c7a24843c8fa44b6a36682f6b7aee6195d6c220cc56ebed91f6402b6430747`  
		Last Modified: Wed, 22 Apr 2026 02:25:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:779125c801b21f2f8b88d4d18c3dff31bca7c36982b89863f586e0271d1a8aa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5307233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb59ab85ee330e51523eea487c879234bbbc01dbd9ef1742ecc95e62681f6f8c`

```dockerfile
```

-	Layers:
	-	`sha256:c87c9a24e135c313e42d3d6207edf10d003c76d9db2eccd312a9dea555d5d70d`  
		Last Modified: Wed, 22 Apr 2026 02:25:41 GMT  
		Size: 5.3 MB (5291286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9329df331ffe27a9dd272e76c7028be11d5fa58493d57a0f750e1e046b8aadd9`  
		Last Modified: Wed, 22 Apr 2026 02:25:41 GMT  
		Size: 15.9 KB (15947 bytes)  
		MIME: application/vnd.in-toto+json
