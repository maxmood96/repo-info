## `clojure:temurin-8-tools-deps-1.12.0.1495-bullseye`

```console
$ docker pull clojure@sha256:e9090e68f1d85781c99728d655ac2e02a801ec4f419743e61610ba39515cff08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1495-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:3cd5918d3ffc51c36b0d8c80d67d700b37a84e1ca771ee001d221344009015b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226552264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57de3e837e8255fc799b42f7418e055d01f49d67b58eb013b70cbda953847694`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6930a8bf16748ee896e7160d547055aa58ca8ae63753ba641fffc34b8007ebad`  
		Last Modified: Tue, 07 Jan 2025 02:29:29 GMT  
		Size: 103.6 MB (103633892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c014534462f1c6420983f4a8fa7d60d604943eab0b6c0875e4c5482d3ece3b9`  
		Last Modified: Tue, 07 Jan 2025 02:29:28 GMT  
		Size: 69.2 MB (69178772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782500d378b2e2f3f70e10d4cb3fec8b4547a06cbfb5cf27ed3cb6fc25c3a55c`  
		Last Modified: Tue, 07 Jan 2025 02:29:27 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1495-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:65ddf66c96982554d0157a37cfbd127f0d25702214537e99d415e231831271b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7341016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b649b56588be9c2597fb51a54706f61de0651f76a6af480c92222b166a191687`

```dockerfile
```

-	Layers:
	-	`sha256:dec78c2298a55f95f1e9c3141293965d914d9f82fc9e7e159b80197eb64b66fa`  
		Last Modified: Tue, 07 Jan 2025 02:29:27 GMT  
		Size: 7.3 MB (7326775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5309ef317c681a666328dcd3a90fcac6a5813f633ffbe75f2224049ce2e398a`  
		Last Modified: Tue, 07 Jan 2025 02:29:26 GMT  
		Size: 14.2 KB (14241 bytes)  
		MIME: application/vnd.in-toto+json
