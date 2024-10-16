## `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye-slim`

```console
$ docker pull clojure@sha256:3de78b7e529d02469a83d8387f4590c7b85a20657c4b6100d0dc03079d8627a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:cfb8d72f331b8db3beb3305f6f60d695311570faa1b1460461d5d7c1301b21f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 MB (193981345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5315840409c7b5b9e147110c2b83ad43486e4808e190e0e01f2c36b6e20b75bd`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
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
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9501221c4feeaae24fc2555013b626aafa4ad6b61ab37903536e2d3bee7d6b6`  
		Last Modified: Wed, 16 Oct 2024 16:12:47 GMT  
		Size: 103.6 MB (103611910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11f4cc18d3a63894bad4b8c66d8e28244b1fecddb34b56bef159e5a6390c75e`  
		Last Modified: Wed, 16 Oct 2024 16:12:47 GMT  
		Size: 58.9 MB (58940190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1f26a2f2b587a4bbeab4e4f27a3300e2c7e6cad679179b51a4a510283c0202`  
		Last Modified: Wed, 16 Oct 2024 16:12:46 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c7715ad79d0dc009c97aa8fbf38addf1357d00b5307bee78100346ddce29a83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5235610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046ab5bc708c6061c209845c4a1a0ee55f892ef2bd0dfa02fe60a5a805d27087`

```dockerfile
```

-	Layers:
	-	`sha256:820e218d923b1ab1073a9214b3e26b7f28c1382c0517a4aded1efe65bab6a0c5`  
		Last Modified: Wed, 16 Oct 2024 16:12:46 GMT  
		Size: 5.2 MB (5221651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28d1f66cfcc4b9c6183c77c3845143e35ff4531acb2268eaa39d0438c67e40ab`  
		Last Modified: Wed, 16 Oct 2024 16:12:46 GMT  
		Size: 14.0 KB (13959 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:50532f2ca10ef5d9dcb0bf24d94850745cec10568b1bc3ab97be89fdec0b7d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.9 MB (191877899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91349f1f4eeb1bf7381f11b97c110e7d9b0f74e0a834b3dffa1bab610afd0800`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
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
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb75fe23968e35e453b89cc8dd158cce9129a4418492f492ec116f1b8ed71cf0`  
		Last Modified: Sat, 12 Oct 2024 00:58:35 GMT  
		Size: 102.7 MB (102729198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5d3b3c1b95f64d8468a23913509bc6d83f742ff63e7437013d66e40fed8d70`  
		Last Modified: Sat, 12 Oct 2024 01:02:57 GMT  
		Size: 59.1 MB (59072897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fec10c386b5f4dd0b4a042c5a353d324b11008b6c2703c35abb55709b8dac5`  
		Last Modified: Sat, 12 Oct 2024 01:02:56 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:13f3de5310639170d5e654e74cc502a3547b5654172f87057af7cfee12d4acf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5242151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356caa7a6600ae791fed3ca9cdb1a65d545beb93c036a98ed38d2a7ebc3e20bb`

```dockerfile
```

-	Layers:
	-	`sha256:a0bfb3a8fc689cf334286f2ee134ccf4513a9cd875f770da164aff68bac2ea8c`  
		Last Modified: Wed, 16 Oct 2024 02:09:15 GMT  
		Size: 5.2 MB (5228087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:055d42b502912f7326387072090909f2e3aea59f635502f158e8cc7ceabc3cdc`  
		Last Modified: Wed, 16 Oct 2024 02:09:15 GMT  
		Size: 14.1 KB (14064 bytes)  
		MIME: application/vnd.in-toto+json
