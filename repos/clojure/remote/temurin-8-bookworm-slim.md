## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:841bcc50c8e22cb0d361669013bb2c81a3cbfb705541a1688212d5a6ae34e898
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2fa994f615bc0ad4216bacb9ac7e4e1af8c79c4f4649167d2898c4878b19f7d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.2 MB (202221574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d0c6d8463b8ef097ed21aa36337b88aaa95ecf772e5b7d38c9b33796214c9e`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9dfafe96eb09e15c806e2de609acb84971f7449df95ce740199d535565a2f52`  
		Last Modified: Fri, 27 Sep 2024 06:01:05 GMT  
		Size: 103.6 MB (103611891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eeb963a012e2e1ec80b0afebf9b58ba6fe885c3977bb8f49037a3f42c542a60`  
		Last Modified: Fri, 27 Sep 2024 06:01:04 GMT  
		Size: 69.5 MB (69482764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b3fc5991232a194dfd60fd426f8005b4edc91bc39309e2d53ebc0a94bfc636`  
		Last Modified: Fri, 27 Sep 2024 06:01:03 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dad5c2a5856545ca1fac54cecb6a55dbe0b105c5c3840700e4a7120c0079c2c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5030937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b052042a754b254584f3167688e0657f9fbcab65c6eb6bec28bbec7e6085fca`

```dockerfile
```

-	Layers:
	-	`sha256:2043211c531ee204a2f34da90895e35631c59d1b944c15366efc86aa2ecdd310`  
		Last Modified: Fri, 27 Sep 2024 06:01:04 GMT  
		Size: 5.0 MB (5017017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19d057a4c49f6f9301187187c02e64613bcfbda0ebe756203b7d0cb376f1a212`  
		Last Modified: Fri, 27 Sep 2024 06:01:03 GMT  
		Size: 13.9 KB (13920 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5a1f42299bb1368643e8fc425d3e04ecba734c992604ea7e32919211378e7616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201231536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3fd5411de97ebd9a8712eaa9ec3079fe49241bf0a8e15c0876a206e4eaecd8c`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea3000ae57057c75bc31c79b58b0e4f4bca72d9ee0d5e26cda89f4cb9540662`  
		Last Modified: Tue, 17 Sep 2024 04:08:48 GMT  
		Size: 102.7 MB (102729254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2be6ca44f458510bc7051e0acc526831e23919c4b5cd317c9ff1657da0a872`  
		Last Modified: Tue, 17 Sep 2024 04:14:10 GMT  
		Size: 69.3 MB (69345091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69494e221dc3308546a9cea3c29ed9b9e92bacf6ebddf29d8c87e952790adaf`  
		Last Modified: Tue, 17 Sep 2024 04:14:08 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e63c449c1f6a90cd2525f6d6a0361dd807e90fabbe2138fec47581f673f0c91c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4791529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de496f5e89b501666df82327b3a1e50efc38c29b9a9c9c2a97bbad9bba41a151`

```dockerfile
```

-	Layers:
	-	`sha256:b4c8a574184ca15a8b8f17ae80863e773b4dcbd97a0ab1a89f55fe7f90bbc434`  
		Last Modified: Tue, 17 Sep 2024 04:14:08 GMT  
		Size: 4.8 MB (4777068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d972396adb158ad13b33753cd21309df607110fa53b86d89f183b2191bfc7f7`  
		Last Modified: Tue, 17 Sep 2024 04:14:07 GMT  
		Size: 14.5 KB (14461 bytes)  
		MIME: application/vnd.in-toto+json
