## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:0add5b03326cc435ea76cdff2d7f9f48b8c70b3e6c649d64a5d7133db783915b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:887f8e5bc0a566c620eb1b8c7ca6d8995f064a54b6a3bfd9bbd5ec297f09185a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226552261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6740a2e9ee31062916e3ce9f258d29f8541b7d55e51e62f6e4730c9179ae0c72`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
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
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44ab2c0dd769b2bf387d56de9cca7dc0752851f6320d1fc6f761f44d1b4dfc7`  
		Last Modified: Tue, 14 Jan 2025 02:43:20 GMT  
		Size: 103.6 MB (103633885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e115ea76505e8a7174cf381537cce07b2432641e7b0e1be9aa44c096eb255f`  
		Last Modified: Tue, 14 Jan 2025 02:43:20 GMT  
		Size: 69.2 MB (69178568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad84f22b321e68dd16ca54a7e608f8fce722ef1229b3b18cc4779ff0f4ec4a3e`  
		Last Modified: Tue, 14 Jan 2025 02:43:19 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:6ae237640aad812f434a56418ea07d86452fae1948c188fa52b9e9dc1caa239c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7341016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:947653c877f1e5e3aa6cab4cf4996cb27b1719045a40ac1b48490e1bc96f94c9`

```dockerfile
```

-	Layers:
	-	`sha256:98ab25bfe71456176b1c65c0d34cf514f1e081af162cced0144b1d8e015dca02`  
		Last Modified: Tue, 14 Jan 2025 02:43:19 GMT  
		Size: 7.3 MB (7326775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e8a2351b0e6681ef70eb3441254ca2863e51f7268447eab30c7dfe77855f3ed`  
		Last Modified: Tue, 14 Jan 2025 02:43:19 GMT  
		Size: 14.2 KB (14241 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye` - linux; arm64 variant v8

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

### `clojure:temurin-8-bullseye` - unknown; unknown

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
