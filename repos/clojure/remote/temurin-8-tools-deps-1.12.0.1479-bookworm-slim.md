## `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm-slim`

```console
$ docker pull clojure@sha256:1522992b5164c3a0ea6d5a53695c53ffd57127d996b54ecc40592f515d21a46d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a53050e6f343ec6416016b11c8841986819a0460e617527fd809dafc3eff739e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201159064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f20da3b59ba98413ba8c37985ecfc6eabd188a1ee9942403f706b51a3fbd92d`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585e257bd30f6accdd3f5fd8f11a6e160953c7568b1391bf6d7c3bee450f2473`  
		Last Modified: Tue, 24 Dec 2024 22:37:01 GMT  
		Size: 103.6 MB (103633884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198b0eabbe8b082f6498d1e4fbd7aaac7763a19604411da186b400cb6b2bf2c0`  
		Last Modified: Tue, 24 Dec 2024 22:37:01 GMT  
		Size: 69.3 MB (69292957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a18d5c5bf399716d796de485e940bc7d1b9165c70e24a4d5dda10e4059f1259`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:85d1cc392e0d047604a4a15f27d833da0f7dae5d6bb1ea581487b83fc2408b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5049020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fed3b2f92e054231185dd06a729b830d890f43c3064aafeb721df229742ea803`

```dockerfile
```

-	Layers:
	-	`sha256:26e8f38ef0fd552d8ff464ccff1fb689405bdbf66dda372568823cea8207436c`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 5.0 MB (5034725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fc0b994344efae27f0a7b26876848fb50c46d94bd30b60111796acb74e5d004`  
		Last Modified: Tue, 24 Dec 2024 22:37:00 GMT  
		Size: 14.3 KB (14295 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b31007b6d9bb3fed1ac47824e926a50f8f4e3f835fdb825b7a79fcd2467e6caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.9 MB (199947371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6fbd5a7605ae8ccc0b99b4b3acd4a15c6aa7c2f2029df7ec98f8b16b35a0f6`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195295c73134e395e2634b149103034a56fd81282c0c9b6d2cac4878f2477e54`  
		Last Modified: Tue, 03 Dec 2024 15:02:01 GMT  
		Size: 102.7 MB (102747754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3222c126fc4983c6d7e0274e43de640f8015bad6a079d15caada44b926b2f1f5`  
		Last Modified: Tue, 03 Dec 2024 15:06:18 GMT  
		Size: 69.1 MB (69140161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4087ef9802834ccbf3f458e229ca75af9b7c5468f9d6cd780d2bd83363e0ac2`  
		Last Modified: Tue, 03 Dec 2024 15:06:16 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2215c7730f92f28410f063b1a41e80285c993b67c380fcf6137c0e146e34177b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5062429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ecfa7627f7ffd0a8663d24ea84e5eaf2da2da8e424af97d0d81866485c8024`

```dockerfile
```

-	Layers:
	-	`sha256:425b2379c2a449eba18c26887efea54e52e2ee449c4dfd2ee10a51d7e02e09fe`  
		Last Modified: Tue, 03 Dec 2024 15:06:17 GMT  
		Size: 5.0 MB (5048015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a47409e3745c81518bd60f4b22964c79e875b21c1bf2ea5b468c807973439ba2`  
		Last Modified: Tue, 03 Dec 2024 15:06:16 GMT  
		Size: 14.4 KB (14414 bytes)  
		MIME: application/vnd.in-toto+json
