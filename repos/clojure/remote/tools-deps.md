## `clojure:tools-deps`

```console
$ docker pull clojure@sha256:3a98c2c3fec78ddc6824e1a9539609c0e126c08a22821cbd7ecc4e772a335da7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:de170242003a929899b30967cde597c513bc6e7babe1b6f05ff11e153a4c125c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287071004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0fbe57affabb3b8eef495e07f80363090a4d21a136842e213f6cc8a7faed680`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340568302177098e131e6bad8350e922db580818728e05509c105e20e4bbfdbf`  
		Last Modified: Wed, 09 Apr 2025 02:19:13 GMT  
		Size: 157.6 MB (157585883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573f0071dc1f32b45ffc395d18cfe979ec92868de9fe53ee65dc027807000ea6`  
		Last Modified: Wed, 09 Apr 2025 02:19:12 GMT  
		Size: 81.0 MB (80993537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da80a085d8d1da96c53f3387432c8a52bdfd616b75c149266c6d21dd6992d4d7`  
		Last Modified: Wed, 09 Apr 2025 02:19:10 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f2fc5c422a121a5787f38c0410c6714623b5dee09c38eb3d7326e7e5f9b38a`  
		Last Modified: Wed, 09 Apr 2025 02:19:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:bf4d78d3a430e837763424bf009264527b0f0c2f1f9159b05ca53fe170b933a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7195399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:518d58b265e1dc09f14ccc83ca4ca70a06efb74610cffe7c0607d7eb422a5f4f`

```dockerfile
```

-	Layers:
	-	`sha256:79724e94dff764dd0fbc13177e9ae309dc43a7b12eb7f94855ac7ffe5b9ee4c1`  
		Last Modified: Wed, 09 Apr 2025 02:19:10 GMT  
		Size: 7.2 MB (7177578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:028bcba8ae854f6abc4f6744463fe984ca8dd4b3dffb1230107fb4d56bd4e9ea`  
		Last Modified: Wed, 09 Apr 2025 02:19:10 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dd3607b576fb7d0e52617d2235bd7aa35f180f28c225d101c718d9f0222601d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.0 MB (285030400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff22fca85d3e00ec045294f257c95a6a516cbbd269485787050b8f2aabe6c23a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c9d1eca0c6f0c11c056bd1a9c0a6fc6af61a9d35f24ad12f42bc4153e746a6`  
		Last Modified: Wed, 09 Apr 2025 17:10:48 GMT  
		Size: 155.9 MB (155859270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab30a8b70d2528ca3c9743bf543a60c16c375e3858f2a11045770d1021e5076`  
		Last Modified: Wed, 09 Apr 2025 17:43:05 GMT  
		Size: 80.8 MB (80842617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312b8e0dbdd1044cce5c303c39ca20ad68b0e09e05515ce5fb4f13987716d914`  
		Last Modified: Wed, 09 Apr 2025 17:43:03 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725f2329e1af2567a1b2753668ce06de2a9de3987e31aa8825c38f42e7ff441e`  
		Last Modified: Wed, 09 Apr 2025 17:43:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:efa7f1f8a375a5cc33693df6af92d3c90f48c93109beb5dca68a5b12fa184254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7201424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b4c4d53747494f5a4accc9b81c1ffb0de0515c5fbc5f5f4261cd131babac98`

```dockerfile
```

-	Layers:
	-	`sha256:7185008c133eebab1f6034b26a49bf988e2f1e0488f2682670c2616c4a02561d`  
		Last Modified: Wed, 09 Apr 2025 17:43:03 GMT  
		Size: 7.2 MB (7183413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52ee9239954eeed38e76914439647052f725a58e334e3a7a73a41f87b292f573`  
		Last Modified: Wed, 09 Apr 2025 17:43:02 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json
