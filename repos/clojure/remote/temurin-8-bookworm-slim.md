## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:18795e812841ce73750a407a1e0278cf93e6c511a19f2b6b3a715189e0c44256
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2b3c00321c5ea064f1563cf63aeacf9e46407e315bc73d9446a97b9d87bb2648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152473285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57df14c54b879228212c0681ff8b77094004d50f8b4f139d04928bd999e6062c`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e506e49a8598d7da159186105445720b31844cf35d3f996cf20827c52188fc60`  
		Last Modified: Wed, 21 May 2025 23:32:02 GMT  
		Size: 54.7 MB (54716184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a8e0a32f4263a3935f4fadc9dcf2bceb47107048bcdd1df47eff36e8bf6f53`  
		Last Modified: Wed, 21 May 2025 23:32:02 GMT  
		Size: 69.5 MB (69531129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40264a65d24cccd8bf759bad1f888456b7bb946a1a758ee5c53237b9910f7c5f`  
		Last Modified: Wed, 21 May 2025 23:32:00 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:54a5795b8bf801b8c418167bca57a2d380b94111fcfabdea3ecfeccef86d209e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b245204900d50b137897511516bb4f3142a9dee53f055b1019a820771e584f07`

```dockerfile
```

-	Layers:
	-	`sha256:4177e7cb7a08da811cfe498c855b7e4ebeb2b4efd8f21859d25e0adfd66f7dbc`  
		Last Modified: Wed, 21 May 2025 23:32:00 GMT  
		Size: 5.1 MB (5083108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c580318946527a3bd63af7b9aff5288fba0658fbb99f64e25939bdf3a696ffbb`  
		Last Modified: Wed, 21 May 2025 23:32:00 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a2680f5183bacea3a5960b1bf488020bdc9fbfda709562067f6bcd97a3f3c7a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151275459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d04fa5d140509a9396ae5676da51a546c16d87988d38f2a83118a1b029da9b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95561fee27ec3c57c777d90b1887be2a2e08f63416624593b6fb5e2e09b86a98`  
		Last Modified: Wed, 30 Apr 2025 00:59:20 GMT  
		Size: 53.8 MB (53830490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd06b14693cca080aa7fb6f128b81a663c30ec1667a691ef0e21c259af0697e`  
		Last Modified: Wed, 30 Apr 2025 01:02:19 GMT  
		Size: 69.4 MB (69377703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa49988e737c9b485e2841cbd6b5d8c789144e9a4198f1c7949f75c78644f64`  
		Last Modified: Wed, 30 Apr 2025 01:02:17 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9e0869e3cc56be7fcc703983674891619a6d3de5620973997f0784adc2ed4c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5056443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701666f31aa933fab6a93fe6b6f66a3809ad8d57ef60a58c5ff303ba9125782a`

```dockerfile
```

-	Layers:
	-	`sha256:a8296b4ee5c5ee1e4f975dc7bbf04bf8675036118530670c2a61b14859306431`  
		Last Modified: Tue, 06 May 2025 00:20:01 GMT  
		Size: 5.0 MB (5042034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83bc91a30c6c66010e6d28a2c8d5a44bd7f7fbe85e555957ef92db8816a7621e`  
		Last Modified: Tue, 06 May 2025 00:20:00 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:1de6e0fff50674d58066d5b5ea4c5371d41009184a2459cb687769339c34c6a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159581961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131fdb0585ae193d0ae52b840b9c0252165bab7b4297901ea926adbb24dc5f68`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0ff21f998b476820ba3e6b42f7da8947c75145e9bf234605cfece8ce02148d`  
		Last Modified: Tue, 13 May 2025 17:58:46 GMT  
		Size: 52.2 MB (52167960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4acd74618dca3940b6aa6c14da546195bff6670502730f6412720a01d976118`  
		Last Modified: Tue, 13 May 2025 18:10:40 GMT  
		Size: 75.3 MB (75344912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffe7529890448cedc121fda2507114b5eba8c2a5c59c8cd09024e9d9cfa8104`  
		Last Modified: Tue, 13 May 2025 18:10:34 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:869a0117421c0c5e1f3a8e0fe9a476a0fbd154e15a464a327b0edc5fc10d1f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5055499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:975047c4f68d05bb8d5c1fe1ff7fbf89579aaed5882d6aa61df1badcfc918a41`

```dockerfile
```

-	Layers:
	-	`sha256:9487b08d26455ea3d417ab1d9a7d0f9d5acb653cab429e020e147c0da2f57e79`  
		Last Modified: Tue, 13 May 2025 18:10:35 GMT  
		Size: 5.0 MB (5041160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41fba4dd4794cfdb50aeb3f0c0cbee6b186515b983c563a5d1457e65a44d49f1`  
		Last Modified: Tue, 13 May 2025 18:10:34 GMT  
		Size: 14.3 KB (14339 bytes)  
		MIME: application/vnd.in-toto+json
