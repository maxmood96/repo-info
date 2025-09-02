## `clojure:temurin-8-tools-deps-1.12.2.1565-bullseye`

```console
$ docker pull clojure@sha256:ffe28c85e0c2d900242097c17548550c2dc81887c5d4af878ea3b91b93efaccf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.2.1565-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:ff9319c318356fb7b010ba12063ec78f9badacf4a0cbd46a4a57982dbf711130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.0 MB (178043879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0648201c439647f467018aad7f2e75cc4314e296f514816e8a2b19feba6b108d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:078965fc7cf303b72cc4eef5479dc2dbf5bc84fb8e6052a89b9b5362e14b3651`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 53.8 MB (53755344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a4e0713c1c0b870472979bde305efa29d921decfab2c962b1c3f46d1562023`  
		Last Modified: Tue, 02 Sep 2025 00:16:57 GMT  
		Size: 54.7 MB (54731323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5cb241c3bef8b502519a5137e63cac94a87022a4aa464f09d8be66980ea783d`  
		Last Modified: Tue, 02 Sep 2025 00:16:57 GMT  
		Size: 69.6 MB (69556567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397cc03ac180031b4a572dd6854c02b9af80504916bf5e88946411e5ffd4e99a`  
		Last Modified: Tue, 02 Sep 2025 02:28:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.2.1565-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:49b7516e56eff9ce0d7ff68adc38229a2ea55f8f454810c9c79c394e645e9ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7531513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424496b08bfb5114d6263a8fb073507c413337110d15516146085635806d1dee`

```dockerfile
```

-	Layers:
	-	`sha256:c0d8a2a778ed0cd096dff2b6895e04ad3fac7ae57d3991d85529ec09d7eef39b`  
		Last Modified: Tue, 02 Sep 2025 03:45:23 GMT  
		Size: 7.5 MB (7517277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c16647c5d8553c584192f757d001b6f18e28015461eb7110f6250fd2feae95ba`  
		Last Modified: Tue, 02 Sep 2025 03:45:24 GMT  
		Size: 14.2 KB (14236 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.2.1565-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5741339bfbb7ef5106db2ade49bf85d54114f69b6f55f5bec2df885625d80bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.8 MB (175768602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b2014474e5cc01462ef89f5c417262ea3772165d113a34d6f0f7c37bcbcb3f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7b68ea47bc3cd8615e51fdbe0976cb4999ba56ce8764e755543a4521d69a32f6`  
		Last Modified: Tue, 12 Aug 2025 22:08:57 GMT  
		Size: 52.2 MB (52248409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c68418c918156697c68aa13e1642c98a2beeadf9646a706b7123bd36165147`  
		Last Modified: Mon, 18 Aug 2025 16:54:18 GMT  
		Size: 53.8 MB (53835632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2f5df1b7038925821c5a1bb27a61a3d582ae1d5d94168268c7def7897459a0`  
		Last Modified: Tue, 26 Aug 2025 17:29:30 GMT  
		Size: 69.7 MB (69683915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7161d2fda7ab8aea5de6d2ca474e00ba9bac843f6583c2c649262df69f0197`  
		Last Modified: Tue, 26 Aug 2025 17:29:16 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.2.1565-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d18cfbc1fe7bc5ba5a95a6e0a1b3f3f551f8b0e79c3d3a68029e379931a5d2b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7537427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae55ed06ccd3e905a6cf3c54692182f9ba200abf5732e884dcf01d085c2cef7`

```dockerfile
```

-	Layers:
	-	`sha256:4e3df5b26ad25295d75b14fe9e7ead34ad4eb4608c623b107e3e2955635f30c6`  
		Last Modified: Tue, 26 Aug 2025 18:44:54 GMT  
		Size: 7.5 MB (7523074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a51e3854c86f98fa6a560aae17457795ee0eec531427dac3e73813081cbc806c`  
		Last Modified: Tue, 26 Aug 2025 18:44:55 GMT  
		Size: 14.4 KB (14353 bytes)  
		MIME: application/vnd.in-toto+json
