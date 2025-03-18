## `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm-slim`

```console
$ docker pull clojure@sha256:866964d490981e79beb89bca5b42f9e208501ea4bc940f3bf5833a674b37a823
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5c58411be3349ad9e8f13d7ee527bfa255b52620a6bfa975591842eed132f0e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242300660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c6d9d2d6ff1c6fa23c986fa088a02bec80dd1b12c8d24a402bdda4d8488cd1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec5fd05d73d6d87e118ad528a4ca3ec6b5a157a74be0954bb9e4e0dc124f6e5`  
		Last Modified: Mon, 17 Mar 2025 23:21:04 GMT  
		Size: 144.6 MB (144566550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b5db7d0b54fefe261b456554a93ae877e0f751a0f2dd8c4858a5edac28b4cb`  
		Last Modified: Mon, 17 Mar 2025 23:21:03 GMT  
		Size: 69.5 MB (69528207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790d468165fb65efddf3f8be4440af1677252de7252030b9a65720e0588d7039`  
		Last Modified: Mon, 17 Mar 2025 23:21:02 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbcca446234764866db96cf59d1256048d799aaa7aa48fa8360425ecee5282f`  
		Last Modified: Mon, 17 Mar 2025 23:21:02 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eae647e3e4b3bc90b612227cfa562251d080f4e9c33aea7ffd7d9d7771b2f43d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4928476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8335652d7c59ddf4cb9b849d78abee704e9ce8a7137117a7f4bde8b34ccf3389`

```dockerfile
```

-	Layers:
	-	`sha256:ce051c2ddfffd7019ca96711ddb0eb100c4350f351c778ebcebbbb1bb34d5846`  
		Last Modified: Mon, 17 Mar 2025 23:21:02 GMT  
		Size: 4.9 MB (4912597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13ebadbacd09b1f45e3daa780628d1c1d0156b407aab58074b072862d756e1e1`  
		Last Modified: Mon, 17 Mar 2025 23:21:02 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f771e52fa7ecc838f064c6c6fd8f94a7712279fcd20f04bb651326208ca138d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240882690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b72174b274125c2182dd6b6f75c32a8937bcc2858b5c2e13335c65bfa055a383`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023fb8ddeb74577aff364f9176a4e554f3cd037752f74cbf43d53f0714c39236`  
		Last Modified: Mon, 10 Mar 2025 18:01:03 GMT  
		Size: 143.5 MB (143454722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2778210d1d31e6d24bccbef86b80b291b63a5e8ce4e6b271ff8e0e9d268ecb`  
		Last Modified: Mon, 10 Mar 2025 18:01:02 GMT  
		Size: 69.4 MB (69378496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3ff78e45cc346fab504ea16b3acaf62147aef1c625a1a1a88ed8071f29e02f`  
		Last Modified: Mon, 10 Mar 2025 18:00:59 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ca5facae939572db1bd8075d0780b4a5f61438a341d65473067ae9c9edbcda`  
		Last Modified: Mon, 10 Mar 2025 18:00:59 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f5ea3bd85c5bfff95f491e4726707417d855baf67dd38c5cfd437789baa7794d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4934342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daedf3100b994bc2ee8bf3ea66df71efe7c36ee53517844e9a7adf990acb2257`

```dockerfile
```

-	Layers:
	-	`sha256:baa09e6141c6b8cf4a265f7800a8c30df0e3c5908fba3a1a1595b090ff8f88c1`  
		Last Modified: Mon, 10 Mar 2025 18:01:00 GMT  
		Size: 4.9 MB (4918346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5ed7f71df313ada77130abfee4129ce715f0b8dbd3a15d6eab6cb405c833708`  
		Last Modified: Mon, 10 Mar 2025 18:00:59 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
