## `clojure:temurin-24-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:f6e2e1ec3a7ed32c57a4eadec372911981a143995b41c91c7b1c826aceac6e34
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:666370c432e65955ae3bb884a3ffe1765e0e03ea2513b0971d6817eda4cf9afd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187706426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8225c1f8a62bce030ee463ddcfdaaa81eb594fd5ad6deaf2f689521489855ca`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b79b1600a276667a6ea3951ffba0e9d2d35aaa6f17a4063126017eb105c3d7`  
		Last Modified: Mon, 05 May 2025 17:08:01 GMT  
		Size: 90.0 MB (89952019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd4ff0f95916def0f58025e549edcec6880a4bc2f7a7142394cd881a7496331`  
		Last Modified: Mon, 05 May 2025 17:08:00 GMT  
		Size: 69.5 MB (69525726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdd9b44e3656b86bc3023173c71c1c261a1ae9afb2710d5fb85f36d2195f3b2`  
		Last Modified: Mon, 05 May 2025 17:07:59 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b18894c48d96379479793126b70812275f7668b33361d179e0e6b0fb0f77a9`  
		Last Modified: Mon, 05 May 2025 17:07:59 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:533ad9571d4929f2fbb4fba55eb48a740c54d265e3adeacbdb9d00cd21d2917e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4880482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488326362cb1d89aedfcf1b92054f73474fcc498bef5bf8289198364c37867f4`

```dockerfile
```

-	Layers:
	-	`sha256:a512f0290190a6d0130a393dc9104f2ee946d9b79bec2354c8f4752e312eef9a`  
		Last Modified: Mon, 05 May 2025 17:07:59 GMT  
		Size: 4.9 MB (4864611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb7287fc6a96c4d346a56318fcfe7a816705bc599fa602d60ff37df8be657a97`  
		Last Modified: Mon, 05 May 2025 17:07:59 GMT  
		Size: 15.9 KB (15871 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:eaec22846005e8dc82590eef471dd56172eb8677812405244086674c74858c49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.5 MB (186536676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74ef85dd1ac6d9a39fc2ec4b381545b2c1b27bf0007e8162f1765b02a68ff184`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd34a4187aab23db272b0b1a8f05c1c712bfae4b9fc1c192607343790479bfd`  
		Last Modified: Wed, 30 Apr 2025 01:50:23 GMT  
		Size: 89.1 MB (89091270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6d96fd8979346f0f9cc60166257e33f62ab25c8955b5449c1d043e6ec779ff`  
		Last Modified: Wed, 30 Apr 2025 01:50:24 GMT  
		Size: 69.4 MB (69377743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bb2b644b28b4a060f04b00637881be61793c2835ffe2aca3d32c53017f3fb9`  
		Last Modified: Wed, 30 Apr 2025 01:50:20 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3dee57edae75636480827485ecb40526f6fbcb1413d963fe7b91d655be8916`  
		Last Modified: Wed, 30 Apr 2025 01:50:20 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:357b59ee40f80900f928a6e8300483cf53e6d024c4149935bb50cfe0045b8ff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4886358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d7e39c9dc54aa193ba04215b4c7c2891a008272f0ffe8fe08a468200119f43`

```dockerfile
```

-	Layers:
	-	`sha256:2d3514da2b11b16f3fea5a6e7faae1574be96b9aa760900d9c0519ce1bd01275`  
		Last Modified: Wed, 30 Apr 2025 01:50:21 GMT  
		Size: 4.9 MB (4870369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c729c3efab063400d924179a310f4ce9fc3955ab51f5a1a9e85f04a5d6af684d`  
		Last Modified: Wed, 30 Apr 2025 01:50:20 GMT  
		Size: 16.0 KB (15989 bytes)  
		MIME: application/vnd.in-toto+json
