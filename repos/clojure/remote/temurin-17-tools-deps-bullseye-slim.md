## `clojure:temurin-17-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:48fa82d0233f5ae970d2299ad2f6ff592e4daaf2cb298b566e270f05010f99f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a45ec85345e67da5a05055e7bcd3ad6ee55260e0b31a17922eb9f9e760843194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233571349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fcecd464796e6ebf356f6d12992a8fc366e6a86144069c01ee091a4ae0a2408`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35538d02efea9e1c6b5b17c32d20f295a37d6c03dd32e488396ee183869125f`  
		Last Modified: Wed, 22 Jan 2025 19:36:50 GMT  
		Size: 144.5 MB (144536751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad873912bdeccced1b8612966e0f9a4076501e2a14095ed0d4eed38680a9fac`  
		Last Modified: Wed, 22 Jan 2025 19:36:47 GMT  
		Size: 58.8 MB (58780896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e81c81720cab6eaf10ad236ec130d962c31721b3a3ff742b18b3b9cda55e1c3`  
		Last Modified: Wed, 22 Jan 2025 19:36:45 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c18f001812438095e01c163f678c1d5a74d9e02ad7a3570f5a9fc690dd7537f`  
		Last Modified: Wed, 22 Jan 2025 19:36:45 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f72159cba3b36c2021e6ff4651ac85e53cf1f424bc1e979bfcdb0ff6a41e1fcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83f53b34bf53e1942f61906dfcf2e9b97d7de9d840dcd8c745a1e37d0f935ab4`

```dockerfile
```

-	Layers:
	-	`sha256:248aacf2eaac4d4f34569535a195a73915c17a02276a8fe743099c28d04cb717`  
		Last Modified: Wed, 22 Jan 2025 19:36:46 GMT  
		Size: 5.1 MB (5117069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e98b5d0b4e02bda06ff1b7cbaff738b2462c1a3927fc1590a7d435a54841813d`  
		Last Modified: Wed, 22 Jan 2025 19:36:45 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b1dcfc242e57d00dace0da09db0beba334faebd0e135b28a9affb51595c4612e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231012067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d624e32e3f525ae80a486dd42e75a5b1a03299026a147f8726f8d7d460c33625`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a9fea114fbd00c11c58a44e09fa8c34763301d9e52a1a548e04722af721c49`  
		Last Modified: Tue, 14 Jan 2025 07:25:10 GMT  
		Size: 143.4 MB (143360959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650e883e98523501333ebcaf2828ee8dbce21f964668a92ef1f610499739766c`  
		Last Modified: Tue, 14 Jan 2025 12:32:24 GMT  
		Size: 58.9 MB (58905155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01963742ddbc9f1e781aeacdb83fb8214ba4af5a1f7a54df7c7fefd93085dd7`  
		Last Modified: Tue, 14 Jan 2025 12:32:22 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2e46dcc71420479b2adf2470327278af4189d83d49caac5c38977a2ea4ff06`  
		Last Modified: Tue, 14 Jan 2025 12:32:22 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b8f8d1e1759e00f636c15bf7a7acd59b902a6be8c62dcf18e546499f1e330654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d531610e284aa0726df381a48e446901d1751963a0dafa55c68bf0156dca4d`

```dockerfile
```

-	Layers:
	-	`sha256:4a5c07652f386da34daf933fd7d727614b978ffdcb6cb9a76f2e46d3ac2d4c87`  
		Last Modified: Tue, 14 Jan 2025 12:32:23 GMT  
		Size: 5.1 MB (5122801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2eb010e0cfc8085be9861cab2e1fe611709b619c1bdefd501177e4c0189a958`  
		Last Modified: Tue, 14 Jan 2025 12:32:22 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
