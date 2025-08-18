## `clojure:temurin-8-tools-deps-1.12.1.1561-bookworm-slim`

```console
$ docker pull clojure@sha256:a14d8b2cb16e927a85db482bc05311eda3ed612f3917189d40430bb04c45368e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.1.1561-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5fad53d04637b5f73032c1d279ca9f9bf35c65eea706084f72c68d34d894ea9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152542458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c963311bdcd2fd29852b29ec46b92dd78bff0f3e51513ac499a39a90015e934`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689d11231bf57282efa352a795e801e6a6ebbc2fd70bf37d72ebf17faf58cda4`  
		Last Modified: Mon, 18 Aug 2025 16:52:55 GMT  
		Size: 54.7 MB (54731348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc487e5895227b7c7603bb1f62a553e200e202f1d5d3f31626180b27f46b13a`  
		Last Modified: Mon, 18 Aug 2025 16:52:52 GMT  
		Size: 69.6 MB (69580210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd74f54446cdbc02bb11bd36488faad72eadfd496097bcdbdd2b78e6dcda7f7f`  
		Last Modified: Mon, 18 Aug 2025 16:52:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1561-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:86fb5e47f2f8d644b4aa88e90311044e17d240d7dc784c34a4b8b2258ca1a252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5247174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b67fa65ed43a92dae3c444176336a0605f30745c616b73881f4e520081436a2`

```dockerfile
```

-	Layers:
	-	`sha256:3d2c377a1f256717cfc4263015df915ce95208e2985a37d6d2a0ed4ec514330f`  
		Last Modified: Mon, 18 Aug 2025 18:44:36 GMT  
		Size: 5.2 MB (5232883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e30fbae7832b5df6a2aebc29ee8083818bd8474fd16af2051828c4a7eb26e9d`  
		Last Modified: Mon, 18 Aug 2025 18:44:37 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.1.1561-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a344566b11daa0b0fb7f9aa5a65dd6267b3e3d494a1a64ff62eb51067f5af1b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151371054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2512bd1c62f4b8c9354eb58dbfc587edf9bf4dc90e86eaa0a56df22310aab57`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3309a7dc8f110067aed1886965f5594bd9140ec2209f48b42b4293811b78484a`  
		Last Modified: Mon, 18 Aug 2025 16:53:43 GMT  
		Size: 53.8 MB (53835631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:180b4a685e2f35b533e0906b56c4b8baa661fa1b5ae71ce6497190b66e74243c`  
		Last Modified: Mon, 18 Aug 2025 16:53:51 GMT  
		Size: 69.5 MB (69452777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0677ee17478fdd45652ebe97a87f3eedbff22fc0d617a379769b56228ea769f8`  
		Last Modified: Mon, 18 Aug 2025 16:53:38 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1561-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:02882c1322d07cb055fcae031a831575b54f4583acef6390976734cff77c9660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5253751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b10eebe78ee399dcba3a8d4435803e2541a090d4e7779e8c1abd9fd3f956e17`

```dockerfile
```

-	Layers:
	-	`sha256:27a49e9bfc86f7284ba07e021ed76e41ef93440c8ea5e807b2dbaa7689b620d7`  
		Last Modified: Mon, 18 Aug 2025 18:44:43 GMT  
		Size: 5.2 MB (5239342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09ba3eb32b3a0ebde7fda55893153f77be04a1536d178c6e6b073c1a57cc210d`  
		Last Modified: Mon, 18 Aug 2025 18:44:44 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.1.1561-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:fd915e1bea8b4df58ae3c5cfad3d52874190345b68124676694ca233d7af60f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159646238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8fa2bb44dd28d7a27d0273ca75f2b165cb96824b53a7aceb57f2702d6635afa`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be65ab5f26e430ea2e40ede7e94ae14496ee1709a03bb8d4eabb0c050a62d0f`  
		Last Modified: Mon, 18 Aug 2025 16:59:44 GMT  
		Size: 52.2 MB (52165423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33826b9aec801542fbbc5ca599c857b2afffa6220a2623e774ad02933eeb68c9`  
		Last Modified: Mon, 18 Aug 2025 16:59:43 GMT  
		Size: 75.4 MB (75406749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc638e764752e23b8065505d94ed328ec1932f95d85641ea12c21655531c9152`  
		Last Modified: Mon, 18 Aug 2025 16:59:36 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1561-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:21872b1b970586853ed9d183b156ed4e6acc8ae4d58e2a78ec9cb819d7fded87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdede7c3e73391ebbce0bfb3166c8cfd94d7df5c2cf122a94b6fbef260ae4c74`

```dockerfile
```

-	Layers:
	-	`sha256:9bb014b346ba79c58411339fb75c0ffc7951a984c680bea47a845054c2cb2fed`  
		Last Modified: Mon, 18 Aug 2025 18:44:49 GMT  
		Size: 5.2 MB (5238634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8ef82664dcd95ece2a4852c3e9954802fbbdcbdf3e5950ba15f28bb50e42f2d`  
		Last Modified: Mon, 18 Aug 2025 18:44:50 GMT  
		Size: 14.3 KB (14339 bytes)  
		MIME: application/vnd.in-toto+json
