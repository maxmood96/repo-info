## `clojure:temurin-8-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:4bac7a3a6e2867cebed15bd3795a34ff86c18fda0e9dad96a0bfbaf422c67d3f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:57e1f026d6115cded3e495a8c092dcf5c0eea9ec2e3de0c3c298fec4e0c40511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.2 MB (202221745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426668fc040ab6c8909057b60fda6ca98d9053acec2544f3c0a7802cf006bc0d`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:47 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 04 Sep 2024 22:30:47 GMT
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
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba1326bf125febc064d95af200e1ead93dc7551bc5d8cc11d2b09642a417119`  
		Last Modified: Tue, 17 Sep 2024 01:56:33 GMT  
		Size: 103.6 MB (103611898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6555ae0eb82bd7e49e3e43c22915b375f2120c1c4981d8a6c18a7fb93de1ab99`  
		Last Modified: Tue, 17 Sep 2024 01:56:32 GMT  
		Size: 69.5 MB (69482716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df46e75f12919524363f4f31e96760260baaee0157aa9d4f57defa279620cd2c`  
		Last Modified: Tue, 17 Sep 2024 01:56:31 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1b39b6414bc2359187d83d80fcba9bb6d107a1ea7babe02058eaf5f34757073f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4784604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90e37f352e00ba607a763a6aabc5f4b72124535379c86dae64547ab774eb62b`

```dockerfile
```

-	Layers:
	-	`sha256:a55976898952719f3b701cf2e0784b77953a51592ae4be7602d2f9917f46a2be`  
		Last Modified: Tue, 17 Sep 2024 01:56:31 GMT  
		Size: 4.8 MB (4770683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13c67dea05d165fe376dd3195d3b143e0f52883c69598ae6f0f81e139cc22299`  
		Last Modified: Tue, 17 Sep 2024 01:56:31 GMT  
		Size: 13.9 KB (13921 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; arm64 variant v8

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

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

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
