## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:a7abd4195d7562c7ee96f346fb1cfbd68607c4594fc1fdb622cfe27174140561
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:d8ffe171823d05ac7e2ad002db542c7d7cd1b62586eefad6969d5a547ed8ceac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275381691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf61ef1646a4b5a244ab7c14ddd25ea22c9745c0e3283d1426d9da6dd8f58e31`
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
	-	`sha256:1806f741e5fa838a221acff1b5807a0c4cddbb935a8b812e19ad87a0e553ea7a`  
		Last Modified: Wed, 05 Jun 2024 06:10:21 GMT  
		Size: 145.5 MB (145505214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f45be0a4723943683a32b1f74c9956ae77a6d6ad50c9375a1f0cbc8474e501`  
		Last Modified: Wed, 05 Jun 2024 06:10:20 GMT  
		Size: 80.3 MB (80299440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc27fbaf49f75245bd805ce5b402387ad594f86edbccced91b4164f3bfcd377f`  
		Last Modified: Wed, 05 Jun 2024 06:10:18 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:264585a204c8907daf3ce290eeb7da2942b493d42592897c5124a8f27f981265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6974481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fb594d524c6a835030ace6613d6c6329dab3b0d96b5798db0e58fe8a518d63`

```dockerfile
```

-	Layers:
	-	`sha256:4afc5383fd7cf50eadbbe0de625cc217abf0d0455d61453e12b4347bb1eb3628`  
		Last Modified: Wed, 05 Jun 2024 06:10:19 GMT  
		Size: 7.0 MB (6960666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a816f3a2cbf6d19e863307e8b9af45ba841e38d96390b5fe9b5f2114aae0ce0b`  
		Last Modified: Wed, 05 Jun 2024 06:10:18 GMT  
		Size: 13.8 KB (13815 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fb884f782991a6bc9d0d32cce29edeb3348a6a1f85f36a9fb3415014c4a05c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (271962913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f8431121ed4466a768de013e086c2ec843b2fc405072aae6fe0f0401555f30`
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
	-	`sha256:66442d4577a2a857519fc8836919bb6ff53950899016113d8484e65ae5cde093`  
		Last Modified: Wed, 29 May 2024 20:35:50 GMT  
		Size: 142.3 MB (142304146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e01ae05d282230a72a407ade1ea87e81894e411434c7994cf3720f6e764cbcd`  
		Last Modified: Wed, 29 May 2024 20:40:31 GMT  
		Size: 80.0 MB (80044730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233ef3817d5cb41b2b9e446f82f0a7873f2408643355c07d97f2562ce7744137`  
		Last Modified: Wed, 29 May 2024 20:40:29 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b463f750aa617de7f7454ac6a7b13900c56ee6ff3d54306aebfcfed63be6325e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6981405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05fca5c02f13806643fbc984722bdd2def0e87cab99505f73030fff925317c8`

```dockerfile
```

-	Layers:
	-	`sha256:4c061f0e8cb671c85765729261674914faa93bda81122d7781fbf75e8ff5a1dc`  
		Last Modified: Wed, 29 May 2024 20:40:29 GMT  
		Size: 7.0 MB (6967054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29e0fa98842327750935a206782b52fdcf70967a47a8dbdea50fbedcef86445e`  
		Last Modified: Wed, 29 May 2024 20:40:29 GMT  
		Size: 14.4 KB (14351 bytes)  
		MIME: application/vnd.in-toto+json
