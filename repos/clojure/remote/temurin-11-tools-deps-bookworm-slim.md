## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:268fa69eefb8a9368ae83ce8f26725e7171ebd17b4d27c4bf34e98807880fe27
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1f16b06d426227edd4b40295f30bd9acb216126c58d2049cbc46c434bda1fe0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243354902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b146f044021e30e8bf4017839f38bba5af5b257f94a7268936e479c7044d65d`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6461cd9f4b90f10911f1bcd967d34ac02edb82932dfde4fac452a2fabfe97bfc`  
		Last Modified: Wed, 09 Apr 2025 02:18:33 GMT  
		Size: 145.6 MB (145598787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cb1598821bf9c4a608709f28525fcaa801eb7304315c332c8716ed8a3a5b7f`  
		Last Modified: Wed, 09 Apr 2025 02:18:31 GMT  
		Size: 69.5 MB (69528212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6ba9917b60413458376477df8410ff251bf3ee6a38b610d5bb2ef9233b1605`  
		Last Modified: Wed, 09 Apr 2025 02:18:28 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:de0ec47243e063160cac5e98636631c38d69b21cba889712e576ca3e050019a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4948416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8adc92312baecfd44d65778ccd736b41c615c0c5048dc510789e0e43f8e702f`

```dockerfile
```

-	Layers:
	-	`sha256:16d1fd6adac56cdb5d9d8662808fae7d9ee30f53be51873cfdca9b6eedafc24d`  
		Last Modified: Wed, 09 Apr 2025 02:18:29 GMT  
		Size: 4.9 MB (4934106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fabdad63f8607e485aade08e5dd7759e79e7befd30144b77bf0b783051843fc`  
		Last Modified: Wed, 09 Apr 2025 02:18:28 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:64ef27805e8e092df96faffe4663e0259b14bb9626f1ec79e42ad395b3a014e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.8 MB (239830818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d29c52322fa05b294cb9e9ddc6786e5e171ea7f3564aaec1460d0b07a8bf77`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697a3f27ad7c4afeee00ac973a16df9c78d363eded18efac5e78999071abe25c`  
		Last Modified: Wed, 09 Apr 2025 17:21:26 GMT  
		Size: 142.4 MB (142385576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d24fc596c913fef126f47cd420af5fa964de98d1569b02f82ffb52be283b303`  
		Last Modified: Wed, 09 Apr 2025 17:25:51 GMT  
		Size: 69.4 MB (69378276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b93e4e89705393623f49219e9324650a493af889e7f4f5413e51868ab8b8c07`  
		Last Modified: Wed, 09 Apr 2025 17:25:49 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:059554fe085d8acaf1a787a613225847be2cfcaa18c46c4530e490bde3d96708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4954913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da0355e019daec667f52f44b0f5ef2a2ec970e24b8d2f0b029460e487b2ba1e`

```dockerfile
```

-	Layers:
	-	`sha256:41cca9f1a977f9838ae46ca22cc2ed9b4c420a77692a879928ac6fb42b3524c9`  
		Last Modified: Wed, 09 Apr 2025 17:25:49 GMT  
		Size: 4.9 MB (4940485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:defabf3c3ccc89abe445f7889a4ace9e54165861b3c1e9a33d5e1212a95103bd`  
		Last Modified: Wed, 09 Apr 2025 17:25:49 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
