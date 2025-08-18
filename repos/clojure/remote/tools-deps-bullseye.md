## `clojure:tools-deps-bullseye`

```console
$ docker pull clojure@sha256:cd47804e4083493f35c861b677cf23e2ff513dab803dfd59bc08d800fb344cc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:30e998257c6dc2ab590209e93a2d27565321507eba08fb5e9fb9febef036cdc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.0 MB (281022277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad2337a8360a8e83540465bc5b344ee81ae769263d6bcbaf6502ceefd6e59e18`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:078965fc7cf303b72cc4eef5479dc2dbf5bc84fb8e6052a89b9b5362e14b3651`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 53.8 MB (53755344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d54afe5fc7c56f3d5c8ac3d6d255e131506d26a56377393d6c3fc215f714c8`  
		Last Modified: Mon, 18 Aug 2025 19:44:15 GMT  
		Size: 157.8 MB (157804778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a5bebfb39c67b3ed83987ebf5626eb7590c164f2eec18395851276a210d96f`  
		Last Modified: Mon, 18 Aug 2025 16:53:26 GMT  
		Size: 69.5 MB (69461112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d399e3dc1e8c510d0a21c9c5b84740132f22f845454d02a1bf8710d019188bc`  
		Last Modified: Mon, 18 Aug 2025 19:44:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f15c9c99ecaf74851d8253146524cdf432ddac37bee2589361a91ea12e1e08`  
		Last Modified: Mon, 18 Aug 2025 19:44:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:35ebdcd3381623ce0878e8cb7348f0a606ed8f817d63808b4e69eb8554dee6d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7415942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8979c6dceab6896362d944bf970382ca78b71e4da05d0207938b381f0e637bd`

```dockerfile
```

-	Layers:
	-	`sha256:c434ef1177fec3a93885132e8dab975b1ddbb9943cc4ad134083556b4f619aec`  
		Last Modified: Mon, 18 Aug 2025 18:40:12 GMT  
		Size: 7.4 MB (7399445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8c412303394fed3edb069cf32a7f22e73da46e054de6dab6be84e7b491f83c5`  
		Last Modified: Mon, 18 Aug 2025 18:40:13 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2bf8b7ea4fa5105a112e59aedb9e8514ff8673b28e6c33373e2fecb97630b986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.9 MB (277919104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb6f8c093bfb755ba9d71246285ecdffffa3ed78d156bfc088a41966142cfe4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7b68ea47bc3cd8615e51fdbe0976cb4999ba56ce8764e755543a4521d69a32f6`  
		Last Modified: Tue, 12 Aug 2025 22:08:57 GMT  
		Size: 52.2 MB (52248409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5040edb8c8b4b578b900bd5351ad845bff5b8df176e4185b63c2ceb4a65cad`  
		Last Modified: Mon, 18 Aug 2025 17:14:38 GMT  
		Size: 156.1 MB (156081250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2192bf508bff1ea83f9f3029f3701050c1be7c6f01c54bd7232a1082c0c9e95`  
		Last Modified: Mon, 18 Aug 2025 17:15:10 GMT  
		Size: 69.6 MB (69588403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09280767d55fd094d267f58242053fcbd6640573c8f02846f09d389e3f8e0874`  
		Last Modified: Mon, 18 Aug 2025 17:15:00 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a54fe15d54ef7f400857fe42b3cc272eb6049236840f3f0e9dce0004e80daa4`  
		Last Modified: Mon, 18 Aug 2025 17:15:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e04a2b92fc18f8662502e8c229c207f139dd4b74d2e0bfcd21514fbad45809e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7421207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9366bcf3ef816e2785f21edb133bef3ecef1d836331bcac037b445a13115fbec`

```dockerfile
```

-	Layers:
	-	`sha256:ea8130ecdf286daca1e33f81e63804643fae33e462957d5598fd3e0d29c59962`  
		Last Modified: Mon, 18 Aug 2025 18:40:19 GMT  
		Size: 7.4 MB (7404568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e53b3127c7e139df2419fbe7f0af483188d883bb0746089f23bbf3d1fc9881db`  
		Last Modified: Mon, 18 Aug 2025 18:40:20 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json
