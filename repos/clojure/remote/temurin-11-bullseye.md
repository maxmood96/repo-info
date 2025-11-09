## `clojure:temurin-11-bullseye`

```console
$ docker pull clojure@sha256:92dfd7465046798b02447545cf10f3037e7902958238391a4bd45a3a78b3e498
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:d4857ba84db013c01f2cc7b100d49706fde4e4f06f5bafdca544c74629c745cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.3 MB (268284685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff87a135dbda339845a4c454a2bcfad619959a6e53c1127e4cc230cd286b926`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Sat, 08 Nov 2025 18:41:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:41:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:41:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:41:43 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:41:43 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:41:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:41:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:41:58 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be2f2b57b7316ad0c9c5163bce22a1fac88b69bbbc5eb2b3106abe0a3ec6201`  
		Last Modified: Sun, 09 Nov 2025 03:13:51 GMT  
		Size: 145.0 MB (144966518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa2d5889c3267346b9a04eca150a2f57d77aae70829e4a312d7723ceac80ae7`  
		Last Modified: Sat, 08 Nov 2025 18:42:37 GMT  
		Size: 69.6 MB (69560826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1aec69259e24aed2b7bc12a629a608b3f1ed826f2261f679753f21e2d4309b`  
		Last Modified: Sat, 08 Nov 2025 18:42:29 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:24eca28b1dfc36df1b5c8164014fa83dd571729754193ff7fa50da74b93b581e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b66d9207543b4e73795a8cae7f3023883f6edccb121bfc2c0f9552845beb24`

```dockerfile
```

-	Layers:
	-	`sha256:d00bdb959cdb81d183ff8ffa70c81b2de5209e4d7b107ad93029fde242c2409a`  
		Last Modified: Sat, 08 Nov 2025 22:36:39 GMT  
		Size: 7.4 MB (7415808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3140fd75cdc2c95bb3eb635be61e74c5a6a594c5864395aa44a15d08b20966e2`  
		Last Modified: Sat, 08 Nov 2025 22:36:40 GMT  
		Size: 14.2 KB (14208 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e80342a807c6f01291fefadcfdc8d666d9033f81a2967884cf7ce5536779c0e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263678679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d1be83fb8016a33cefc77b9d16d25e4a7e31fb348c60588127072528d80df5`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Sat, 08 Nov 2025 18:41:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:41:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:41:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:41:26 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:41:26 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:41:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:41:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:41:40 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275e2011133835631fcad01a9f2e275f3adc5fd72aff69d0aec8fbbe6d08488e`  
		Last Modified: Sat, 08 Nov 2025 18:42:07 GMT  
		Size: 141.7 MB (141731669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0114506ec498ef853dcfdb52a616d8f358b721b51497396f5cb38e07ba8129f3`  
		Last Modified: Sat, 08 Nov 2025 18:42:26 GMT  
		Size: 69.7 MB (69688396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d354e1c35757a71ea6e485c8bcb8a717972c9bf50e8345c6786d16fe5c2cd1b`  
		Last Modified: Sat, 08 Nov 2025 18:42:21 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:026abff036415a4209c9bfa1a3d79809f21492bff89f0e7a7887742f4df6f377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c444af997d2fd28eda2aed7c4f869f55b7fa94345188a0665e30ad4d52a967df`

```dockerfile
```

-	Layers:
	-	`sha256:8d85ac32f0d6a625e5f7c5b543d06d746c667ffa4c2968c01eb599a77b77e33a`  
		Last Modified: Sat, 08 Nov 2025 22:36:45 GMT  
		Size: 7.4 MB (7421525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b1555649ae60655dd5bbc51eca659ad5e0ec5189c93316fe777b00ffd23c5d9`  
		Last Modified: Sat, 08 Nov 2025 22:36:46 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json
