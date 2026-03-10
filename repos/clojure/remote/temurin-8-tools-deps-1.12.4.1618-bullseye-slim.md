## `clojure:temurin-8-tools-deps-1.12.4.1618-bullseye-slim`

```console
$ docker pull clojure@sha256:45d9f034ac88b3f8811fdff23350063411bc0aa0ea6f9e5b84b041021f08af0c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1618-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:886354780c95aaab57387fae540209f846dd9a79968421f7c5c3d0cc0d3fa5fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144612564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df490865cd7ee77a16d3e442c45e49eca3a989f47ed4211957e8bb771bd0c4c5`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Mon, 09 Mar 2026 20:33:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:33:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:33:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:33:51 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:33:51 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:34:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:34:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:34:06 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:34f0642d22440b5813561cd4375937013bfb556bec8ff3b0e208699b786282a7`  
		Last Modified: Tue, 24 Feb 2026 18:43:06 GMT  
		Size: 30.3 MB (30258379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d573dde1f42755420f4828b8daca1ae68d199425af3974015311ea9c1202d5c6`  
		Last Modified: Mon, 09 Mar 2026 20:34:22 GMT  
		Size: 55.2 MB (55170084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6adc65aa34bab005463cfa5465675e43b6ffdffa9ae7273508cd5c3da2bfef2`  
		Last Modified: Mon, 09 Mar 2026 20:34:23 GMT  
		Size: 59.2 MB (59183454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f668d63325a40ef8f5efd3f4324cb18da274c59dfd544eb5ffe5e4affdf16d1`  
		Last Modified: Mon, 09 Mar 2026 20:34:20 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ba19e157fb82bf8b04a57d2867e2666b3e213fbb103b50840b46edfa51437a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5456911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23fc46cea82838034258c4f776df18c45b270008762d126d58750df576e83df`

```dockerfile
```

-	Layers:
	-	`sha256:b0910448469099714b074b4564bdc881559d891aa0626836c92d688ee9c3c42f`  
		Last Modified: Mon, 09 Mar 2026 20:34:20 GMT  
		Size: 5.4 MB (5442664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e425727ded4f9bb81fe5404aa7900b12fee3c2b35f4260bd559fc0020eae6bcc`  
		Last Modified: Mon, 09 Mar 2026 20:34:20 GMT  
		Size: 14.2 KB (14247 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1618-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:90a7d8809a771d9996b8610660f6822c429be320a646ab0dcc375e3f1f19690b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142320336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d4eb00eaf1634e18e27313bc00b23777004fe8adc934a460e027ec90d10e2c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Mon, 09 Mar 2026 20:33:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:33:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:33:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:33:32 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:33:32 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:33:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:33:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:33:47 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:018c0693c4a2532e5636d6115333db6d882da8f33f1f40cb3e88dbe62da21aac`  
		Last Modified: Tue, 24 Feb 2026 18:42:36 GMT  
		Size: 28.7 MB (28744470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427e6555e05e2ae5142515ba87566ff69c9285e45cdaa456d4c1798134d7e297`  
		Last Modified: Mon, 09 Mar 2026 20:34:03 GMT  
		Size: 54.3 MB (54251614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c66a180422e92c24b4d9f71a497602c72a3073eff824694d404a9bdd40b4ad`  
		Last Modified: Mon, 09 Mar 2026 20:34:03 GMT  
		Size: 59.3 MB (59323605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13a8278b42ce34351a95974adb23ab30940f1c86f4e252814ec9a690c4009e3`  
		Last Modified: Mon, 09 Mar 2026 20:34:00 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0212d12782a1f807d323a9e7aaa4f100c0ad0b2fcc6352c770f206551429bcfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5463462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a07349353110ad3257f67340e84ff3811cffc8015aad5c0cad6c8304b353854`

```dockerfile
```

-	Layers:
	-	`sha256:8c130b9a802be5e0a5354f5e83a1ff5b794771d596101f27be586c9d06d788b1`  
		Last Modified: Mon, 09 Mar 2026 20:34:01 GMT  
		Size: 5.4 MB (5449096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6d747d2d68ab5543c9e647c27ff7eb3cffc78d204fc47ae07a155aa7a928e25`  
		Last Modified: Mon, 09 Mar 2026 20:34:00 GMT  
		Size: 14.4 KB (14366 bytes)  
		MIME: application/vnd.in-toto+json
