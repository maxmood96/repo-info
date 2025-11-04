## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:8de6b2b5b3b2921da3010f221e13bc852ff6f35e0e99eabb715500c9868a4559
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:4682c6a157eafcea489429194716d7351f5bfee488f8a109254f7f822b702308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.0 MB (178049446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7351a9e17222460c381d0d8cae1213fdc2dfa433a04c17cf66d979db20f4a6f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:53:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:53:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:53:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:53:43 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:53:43 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:53:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:53:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:53:57 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b83644c3a315653dc4599f38f7fb025f404364a5c6c9634e3355dc600f27b0`  
		Last Modified: Tue, 04 Nov 2025 00:54:36 GMT  
		Size: 54.7 MB (54731291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bbc954fe8a911789ec005566d6878e33c4411656797e89497f0a2ef850fabd8`  
		Last Modified: Tue, 04 Nov 2025 00:54:39 GMT  
		Size: 69.6 MB (69560817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33168d87fe76ca0ded32b0aa54a085dddb0293d0e90da8bc441f257fdb7d389`  
		Last Modified: Tue, 04 Nov 2025 00:54:28 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3c9ccbd980b670ec07e536d2ccc4949703ce044c97713ae1c5dfd64105bc3d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7531469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd30a4c3aa760fb81b9059f1548edc0bd087034205a1f873c60170cb1cd92e0`

```dockerfile
```

-	Layers:
	-	`sha256:de3e2eab998cb3352a9a67be56f584a52ea78a91b4c31c0e1d2e5f6ff240ea3e`  
		Last Modified: Tue, 04 Nov 2025 10:47:50 GMT  
		Size: 7.5 MB (7517277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:537d86ae7137c01896e808b3f111aa9a165cb362e956be5deca996567d281a50`  
		Last Modified: Tue, 04 Nov 2025 10:47:51 GMT  
		Size: 14.2 KB (14192 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:231a06a1846ae07fd229958bdf5f31bae80115cead1e918a08b48934d0dcc2d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.8 MB (175782493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6c23c6c49ecb8a4ae689d27221cee59b92dd502d20832f61be445b45aa41d2`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:54:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:54:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:54:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:54:09 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:54:09 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:54:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:54:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:54:23 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a45fc8002e3e133a00211e680064b8761e9275048802d2d9e23c8edbc2903e`  
		Last Modified: Tue, 04 Nov 2025 00:54:56 GMT  
		Size: 53.8 MB (53835578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e551d0b35ec7cea8cf7633a99af84352c85d55324ed771a1d76da540ff2e5ea`  
		Last Modified: Tue, 04 Nov 2025 00:55:00 GMT  
		Size: 69.7 MB (69688302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa16854a8c6671facd407cd78a5a0a392299cbc3167be97d70fe7e818083586f`  
		Last Modified: Tue, 04 Nov 2025 00:54:48 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:52132ae81df6088b8fcab27535efcddad95417985aa4436fdc026e6661b0fdfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7537386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfec4205eb3936b2fc417124b3e448a2938937fcf296dba3c0d5cea5365a58dd`

```dockerfile
```

-	Layers:
	-	`sha256:e87aaf24b479fcbd7b7f12590e6dce327ee7001ec36925f44e00cb1828d39047`  
		Last Modified: Tue, 04 Nov 2025 10:47:57 GMT  
		Size: 7.5 MB (7523074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dc3da7a83a2341c1b264daef734794eddae1448ac1ce01598e41044a98cdfa9`  
		Last Modified: Tue, 04 Nov 2025 10:47:58 GMT  
		Size: 14.3 KB (14312 bytes)  
		MIME: application/vnd.in-toto+json
