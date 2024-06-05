## `clojure:temurin-8-tools-deps-1.11.3.1456-bookworm`

```console
$ docker pull clojure@sha256:b61f71d745a89d56f488f7f9c96f8f87da3abcd8ab2704a69c2b853a67d510b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.11.3.1456-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:1656686516aa8f6f77eb19b6727642796970b7994c78f9785334bfd7dde4089f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233475948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3201dff2da2cd86b294666ec873ed77e92f11aafa3c1ec049324efcb69e4ce5c`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f28176026b7610ed955787195c16f28a97a6e54b94da8ea7264f6d643d8806`  
		Last Modified: Wed, 05 Jun 2024 06:10:01 GMT  
		Size: 103.6 MB (103600229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ccb12b625db845f19d334b6e82045e6305f0f088068da7ef0176f2056c8f5b`  
		Last Modified: Wed, 05 Jun 2024 06:10:03 GMT  
		Size: 80.3 MB (80298681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a1d4b488c65ecb0af4424366bdd521fda04d0ef1b57f898e4f8afcc05cee98`  
		Last Modified: Wed, 05 Jun 2024 06:10:01 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.11.3.1456-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ce5e7594bb3187ca595e5edaacaec8453570d69b47fb8d8b5de4251e5f98ea0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6996956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103ec60b33019f4669a67a45b329c22c6e0d231d6c376f123e50752c0ccf7184`

```dockerfile
```

-	Layers:
	-	`sha256:491dd50f52d001717f20225146fe67bc17495d176e126afc3ed3173bcd43db04`  
		Last Modified: Wed, 05 Jun 2024 06:10:02 GMT  
		Size: 7.0 MB (6983154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:927010bd102c7c7cb8b769d2623ba708a14fdbf41c24f428043357ca1a4ea399`  
		Last Modified: Wed, 05 Jun 2024 06:10:01 GMT  
		Size: 13.8 KB (13802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.11.3.1456-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b79163c04903f55239b95bc5ccfb71124b63954ded8a2e2b75452bc15dd20a35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232359324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6279665e2f448d5d2bd8868bf52ca7e08b8650b91353060df699c5cfcdf9f571`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 00:39:32 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Tue, 14 May 2024 00:39:33 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429513d912c66c681705c8aa16d730a4b71c1cd1e40db844d161cca11cced3a2`  
		Last Modified: Wed, 29 May 2024 20:23:52 GMT  
		Size: 102.7 MB (102700444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67eb69a4e3c98e7b586f4515ae0755952b06cc932ac71d89244c8fa0972cff6`  
		Last Modified: Wed, 29 May 2024 20:30:21 GMT  
		Size: 80.0 MB (80044843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acb077a3957361c57c3034c62d84f0f2ad39b014511f424caa93eb867900255`  
		Last Modified: Wed, 29 May 2024 20:30:16 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.11.3.1456-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e990660b82a1fbee7fe250bf002bfe48248a6884c789d230f5d6ea9f3d90ff0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7003879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46301d1c5ae2c2f15a0aa41a9ee8fa2e17b328f87ac227fa81066d18550e417d`

```dockerfile
```

-	Layers:
	-	`sha256:8758c8e7b09d0f4ff148a0dfcf334c10534c1397544a5e58a504e1008910049b`  
		Last Modified: Wed, 29 May 2024 20:30:17 GMT  
		Size: 7.0 MB (6989542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d492eb3e7c52bf0857f9e0f8ccf34cd64c087c5525cbdf5c695221b00b72ab93`  
		Last Modified: Wed, 29 May 2024 20:30:16 GMT  
		Size: 14.3 KB (14337 bytes)  
		MIME: application/vnd.in-toto+json
