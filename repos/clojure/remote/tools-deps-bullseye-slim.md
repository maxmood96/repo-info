## `clojure:tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:d12dbd47d85073034ecea5d621e31959a1d11e55f60855c964b7dafdc3192ade
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:005ca3913064d6a3b4bbfc6ad2054fabc3b831b8e4dfacf7d84722dec35ffc4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246897385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e46eb5ecf7c17aa07206c8f9444048e86ebf39eed48eea5b157c59a5c66314`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03af077612f84a578bdbdb482d2afb41dccce23b628e7d5da92d969b9e38eda5`  
		Last Modified: Tue, 03 Jun 2025 18:24:15 GMT  
		Size: 157.6 MB (157634503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591b91b54266290e67e1a9fd317209156dc9cf63cabfa6629ee2e6f68b1cf8d4`  
		Last Modified: Tue, 03 Jun 2025 18:24:14 GMT  
		Size: 59.0 MB (59005903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04586adda0d266910ce3b91b3692c6f8440d75ede9a1374ffead9dbd1d76f4d8`  
		Last Modified: Tue, 03 Jun 2025 18:29:50 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d76604668873fe5d090476c36f4f67612e813a075e15c3dbada12580da19725`  
		Last Modified: Tue, 03 Jun 2025 18:29:54 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:27343d0442b0a1515c355a367957d1a85c4c8e3f0469b902ea9cb5006fcc8ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5188959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2621bad897ef1801407a30e5c94b3de0793c2ea0087b5b68124874f0430661`

```dockerfile
```

-	Layers:
	-	`sha256:87dc0357dfd1e7c69bae13f6af450b8b5308829ba803b7563e5770a1d2d01834`  
		Last Modified: Tue, 03 Jun 2025 18:38:55 GMT  
		Size: 5.2 MB (5172384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5161b8a1693541bdb290dfeee8d1ad4253d769b5619e40ca102198c0d1157e3`  
		Last Modified: Tue, 03 Jun 2025 18:38:56 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:84868826601cb8e41ae51e848785a0a95a082f506ebc4dfad46342d5e6026bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243805037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3010a41e1735e9b9d29a0bd173e4cb5f0e3087b275d9fc2b33acda9e2709f951`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c27f9d6798235ccf5e5f695d350773cf03adc77fea3cfc1049c69b79bf7dba`  
		Last Modified: Tue, 03 Jun 2025 13:32:50 GMT  
		Size: 155.9 MB (155928816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e9420a5f9ed8df5c035d1ca62ca183ae207052d1bdc424b89cb01b45151524`  
		Last Modified: Tue, 03 Jun 2025 11:00:56 GMT  
		Size: 59.1 MB (59128924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d9d31f9924011e524e2f35e39d510a8c158a4116273fdefeafbab47ed9ec99`  
		Last Modified: Tue, 03 Jun 2025 11:00:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e72a80061208c8cb384b948487b8f17f5eafa753b293f0396d9d12a55794f60`  
		Last Modified: Tue, 03 Jun 2025 11:00:54 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:02e929e62a9003436d2ba0b15f1a543f5613b4eae6dc4c26e469fcec1e108b60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5194857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e799d5c931dd6abb3cf3a197cc1e5863817a628b6ac5c5e3c8739528c9e25603`

```dockerfile
```

-	Layers:
	-	`sha256:22a2d740355abdb291197ec04efb14a18d9fdd0dd4826c0052b76b0f42fbe552`  
		Last Modified: Tue, 03 Jun 2025 18:39:02 GMT  
		Size: 5.2 MB (5178140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adb5a5bea0968d30708cdbfb6398a024a573840249dd6a423ec544b5e1cff284`  
		Last Modified: Tue, 03 Jun 2025 18:39:03 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
