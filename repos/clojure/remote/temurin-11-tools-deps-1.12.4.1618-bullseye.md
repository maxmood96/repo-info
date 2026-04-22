## `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye`

```console
$ docker pull clojure@sha256:884aee252cc962725815670b972aecfb42989dc729de21795e48972c3414d7d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:d88062e028bfe7d3823c7eb895a9196250ef9060fd24e68dcd974bec259ac94e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269167948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6938229761a721de003592f9abbab11e2cf3d3d0912b47f8f742b2e7adc36ebe`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:17:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:17:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:17:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:17:26 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:17:26 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:17:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:17:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:17:40 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96b195992091980f263f8ba3f44c01b2093e1fe98f34a70079f5867d24f48d2`  
		Last Modified: Wed, 22 Apr 2026 02:18:02 GMT  
		Size: 145.8 MB (145806832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89cf174267d8cd21318674404a533749e849d0ec81c23d2496c93a4d79a68a5`  
		Last Modified: Wed, 22 Apr 2026 02:18:00 GMT  
		Size: 69.6 MB (69597319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333050867e63a134f20c102f21daf79d4243ab6a40e95edc1a9e473f4536f34d`  
		Last Modified: Wed, 22 Apr 2026 02:17:57 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d4bad329e779918d6b2a0a9d2cc2bd9716a38d3b4d3b1694becfc0d7644f5693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7442003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f0c2828eafcf69a0d1e5d14f6d78bd200853e12e6afdc2fe669d12584636d0`

```dockerfile
```

-	Layers:
	-	`sha256:fb020154e09808562b1064fc09870e97c324687776d30ece192edf993db0d6e1`  
		Last Modified: Wed, 22 Apr 2026 02:17:57 GMT  
		Size: 7.4 MB (7427794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:645c664fa4ad270f2dcbe62aecc232ecd0358efd0495555e1ad4acc91d15311e`  
		Last Modified: Wed, 22 Apr 2026 02:17:56 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:66519e9330e92ffb7138edb76728a99a64d65f725ef46d9e847c7db80b99992a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264493114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ef5734ebcda898a64d8db5edb68c161d781fc26a0a8b0f9d64dca50acb1165`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:21:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:21:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:21:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:21:02 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:21:02 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:21:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:21:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:21:16 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8264133c78629ca956d7a8adb4df8a3b76ad66f18b58c3a1136dcc467e37377`  
		Last Modified: Wed, 22 Apr 2026 02:21:40 GMT  
		Size: 142.5 MB (142500803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae1be4c5afda5ed48809d771485d30b30d5e6e6d7fe7ad800ec0fc54421ac97`  
		Last Modified: Wed, 22 Apr 2026 02:21:38 GMT  
		Size: 69.7 MB (69738666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46fe150de87c5636be407a82aa9958b78150c0fe715dde0e94be9891d9ef797`  
		Last Modified: Wed, 22 Apr 2026 02:21:35 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:127d1486ca5fc2ad1869ef365a33e2de3ab419be8b4b48264d39a7365d1f6120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7447838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e27e2dd529eddc19182f766d13008817adfbf05f2122b407f9530115a026fc`

```dockerfile
```

-	Layers:
	-	`sha256:9d92ff28e04fccd7276db9e029e1511fe2642b280eb9e99a93097bc8bb13d6e5`  
		Last Modified: Wed, 22 Apr 2026 02:21:36 GMT  
		Size: 7.4 MB (7433511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:469bfd6e78be145b1d72932b802a3e03a754164b4a31c09c47871aa567c09f67`  
		Last Modified: Wed, 22 Apr 2026 02:21:35 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json
