## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:5d36d4bcd90d0008fafd2c7ee1515062230a60cd74eae397e07b3e45c4cd3679
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:8deb1da704e5a05ac6f4bbf6f03f3fe3aa0084740d3c3e9c231a2c3823cf99cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178520862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee4a9ddc20adf008eeb41f2481421b4c56323652172f0e9643eea833d5b6b30`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 02:56:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:56:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:56:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:56:17 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 02:56:17 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:56:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 02:56:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 02:56:30 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e759575b5b0029fea51256b7ad3afa90c8ff1a6a9457787359c2b05b4a964edd`  
		Last Modified: Mon, 16 Mar 2026 21:52:53 GMT  
		Size: 53.8 MB (53762481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3172ac945ae7fbdd0b6f00743a4b6f4675bcf180014269ba4cf1e5988221d8e2`  
		Last Modified: Tue, 17 Mar 2026 02:56:48 GMT  
		Size: 55.2 MB (55170145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbec9ab230064958b9b286c1fcc50a028ea964a65cf0a10f3fe2b4ad0da3b91d`  
		Last Modified: Tue, 17 Mar 2026 02:56:48 GMT  
		Size: 69.6 MB (69587592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad2b3c03ba85e6e8e963f68fa7faf99e35585838fdef0988275bb28b62bd32b`  
		Last Modified: Tue, 17 Mar 2026 02:56:46 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:be69297f489ba2946c567ee6e8adbfbb819ee8329a4e3b0d642129ad41a0e3c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7542831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc2d81e2377e0a008ed6c5364f71776826affcea4e89bfe98fea65f2cfe248c8`

```dockerfile
```

-	Layers:
	-	`sha256:484280bfcd63541bb380c7a4bdd6cbac59f2c4ca61b597c11199a42b378bad8b`  
		Last Modified: Tue, 17 Mar 2026 02:56:46 GMT  
		Size: 7.5 MB (7528640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a68dbffc46526de747d690a646c88a5ad3e7c7904ad24f97b3fbe894dcf85178`  
		Last Modified: Tue, 17 Mar 2026 02:56:46 GMT  
		Size: 14.2 KB (14191 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c8e54586268cd351e77b1a7b37fb4e17afc66c902429f19b7e39bc7450dc0501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176228099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb447c94edd5320ff14591e20503a6f7fa347f102c61a1edf75c37ef5128607`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 03:00:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:00:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:00:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:00:25 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:00:25 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:00:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:00:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:00:40 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:da8e260297fdb91b3f012b26dd982feb43d0bf977ff8adeb7a850ef9c5829770`  
		Last Modified: Mon, 16 Mar 2026 21:52:51 GMT  
		Size: 52.2 MB (52247254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57a2e70f555a1acf58643c66dbad8d72f33333bdf628eaf6dcab0613b5030eb`  
		Last Modified: Tue, 17 Mar 2026 03:00:59 GMT  
		Size: 54.3 MB (54251621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4028867c94f57b0342606bf385a8389ba7a1f844e211fa445b202faae8d163`  
		Last Modified: Tue, 17 Mar 2026 03:01:00 GMT  
		Size: 69.7 MB (69728579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475a3d99846d75def37abb6906cbfdb286ca159b3e18dc9efb26bf4320f0b36b`  
		Last Modified: Tue, 17 Mar 2026 03:00:57 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:22b085bdb1aef4eab2eef855020506ab1fb7489571704865bae1635a1f36aac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7548751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeef89a123c9e46747211be8488c2cc0892ecca4395d21d825e30ded4d0b8342`

```dockerfile
```

-	Layers:
	-	`sha256:ef86e34e8ba32a3324cae514e75c036cebd1aca2c3cf6b1555ea7f229fb54989`  
		Last Modified: Tue, 17 Mar 2026 03:00:57 GMT  
		Size: 7.5 MB (7534439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fc9e2d9f4c8c46b563ed72a95a90c9b58c44fb0de13671b3503b3c5a03154bb`  
		Last Modified: Tue, 17 Mar 2026 03:01:01 GMT  
		Size: 14.3 KB (14312 bytes)  
		MIME: application/vnd.in-toto+json
