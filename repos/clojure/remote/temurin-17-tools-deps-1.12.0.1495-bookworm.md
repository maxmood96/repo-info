## `clojure:temurin-17-tools-deps-1.12.0.1495-bookworm`

```console
$ docker pull clojure@sha256:3f59a441ea4d86f124a72680a190afc4782a30442ea7b96dcfbe51978aec9a97
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1495-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:eaa88ff4c424ea3cca147123e0225a2e490f18356525c23114892b998c1ce4bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.0 MB (273996054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de347b7778ca320e87cce8270b04f9deeda73fe76aad98fb0b74f2048a3ff884`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab75fecdedba29b81e0233b249de0903d026e9c06b8e2305d8e486a4be12ac8a`  
		Last Modified: Wed, 22 Jan 2025 19:36:51 GMT  
		Size: 144.5 MB (144536751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a96c402f0e67de0dc87bdd6283888666ac799eb97147acc16f1dd6d57c65ce`  
		Last Modified: Wed, 22 Jan 2025 19:36:49 GMT  
		Size: 81.0 MB (80978298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93af93ccc20de5950dfd24c0a78a46a2e1421ad8da98aa5eba44642b9b5e5d22`  
		Last Modified: Wed, 22 Jan 2025 19:36:47 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddd1ce9a11e6b468bcb5006e2d3a3a6158ebcc46bd1a68c86cc5487ec07f103`  
		Last Modified: Wed, 22 Jan 2025 19:36:47 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1495-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:150b77a98f75584fc2e1753556339151f70c387db9d5a9158a501a7925e12bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7186901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e7f031075258e2f173bce6c6f6be1da80804abc7111fffed8d4c1a8e83e461`

```dockerfile
```

-	Layers:
	-	`sha256:ac692bd36823660439e3831e818199220826ad2597a1d714a5381236155b14b0`  
		Last Modified: Wed, 22 Jan 2025 19:36:47 GMT  
		Size: 7.2 MB (7171080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:704164114c0245a66af261768d2842bd24563a8efc4fd588972c818aa03ebbd0`  
		Last Modified: Wed, 22 Jan 2025 19:36:47 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1495-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3dfff741c7039b9aecb83d423f7ca5c243b8eb3d79160de8ab2e7eb1c31c230f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272494889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf3b92af67c5e0792c20123e42684675a454e1179d07cd1bc52a978770d1d73`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947bf59c3a98883a7ccfecb5a4185a268dc485dd6f84c20120ee1b840a307dbc`  
		Last Modified: Tue, 14 Jan 2025 12:26:54 GMT  
		Size: 143.4 MB (143360983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095f266f69c8ed60e7b7c556bb2e085d4a238cb721a5df72ce398672e2729dc8`  
		Last Modified: Tue, 14 Jan 2025 12:30:13 GMT  
		Size: 80.8 MB (80825974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969700f6607eeb0adb772950ac203ed5a0720557b8120c91d045517a81273f26`  
		Last Modified: Tue, 14 Jan 2025 12:30:10 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5814e54171a625bc46d1a152db9b8e98abdc5ee26416c0a1c81c8ffb861200f9`  
		Last Modified: Tue, 14 Jan 2025 12:30:10 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1495-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:74edafccef57ac3d26b632932e7773834fd4c26c967ffa8f763f3a02b9a16091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7192782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0be29accd4a4b92516bb8d1250a1ddbd80f473e2832e2685066d09e0d87d5e51`

```dockerfile
```

-	Layers:
	-	`sha256:ed3795dd69867743617ed94e977a90d91267526da4e614feec9075f440a685e4`  
		Last Modified: Tue, 14 Jan 2025 12:30:11 GMT  
		Size: 7.2 MB (7176843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:167563c69941846c5a89f2a546d51555f0851f1617afe4c388644b08271f8946`  
		Last Modified: Tue, 14 Jan 2025 12:30:10 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
