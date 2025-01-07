## `clojure:temurin-8-tools-deps-1.12.0.1495-bullseye`

```console
$ docker pull clojure@sha256:3fb975081bdd9058c3b0c24c10f46ce9edf613aa3beb9ad7dc429e9035beecd9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
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
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
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

### `clojure:temurin-8-tools-deps-1.12.0.1495-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1b5480758e1e2b82b5c2e0455616594836283f220152a1794fb30c27bca88a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.3 MB (224298419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2ddd7129da21ca779105045801bf4598a7cd3fc122b764ae9dc8b53ed4c95b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b800810d94f2437b1b4b09be721d9d61a975b92a33a41f099a3b069911fc2d7`  
		Last Modified: Wed, 25 Dec 2024 07:13:01 GMT  
		Size: 102.7 MB (102747715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db4bbebfa3c633a63580f95740886da879c5b04d7e3d4150ce3aa26ae919b234`  
		Last Modified: Tue, 07 Jan 2025 03:18:25 GMT  
		Size: 69.3 MB (69304363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4132de732d19435e82e3cfb73f9d12c0f843f433abde43005dbaad0af74d58c5`  
		Last Modified: Tue, 07 Jan 2025 03:18:23 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1495-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f2d145c43092824b3ece7a37ba532b8c73683d19c8e0799157188916e2ab13b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7346932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0842fd60f969fcf77b4c8045fe0264f5e33c4ab49aa7d11f7a541ba3fbc5d56`

```dockerfile
```

-	Layers:
	-	`sha256:0c00bd9238b7b126e2eb4fb09c9473ebb75968d5af6fa15b38137c3d9a027b9c`  
		Last Modified: Tue, 07 Jan 2025 03:18:23 GMT  
		Size: 7.3 MB (7332572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d3a9c0d24200f14b6a1353d40a4e992b5a37157f19178885c746ead1908a119`  
		Last Modified: Tue, 07 Jan 2025 03:18:22 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json
