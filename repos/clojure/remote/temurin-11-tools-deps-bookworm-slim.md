## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:0fb315146649785d0234f319749c7adfbb2d71412cf8dc22e1026a5f37cb5004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:bfa3d483eaa394f8263a8c39b424ebbff25d5abf138336875c3fe55e48feb72d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243454911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f1dce350c8f7de1f7a30629b0a82adaaffd579b23b18b87b458a58fbfd0b2f`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:52:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 04:58:38 GMT
COPY dir:7cbebf37ba11e5c859b49d766118c0899546d922ac426dfa1230f08ebde784dc in /opt/java/openjdk 
# Thu, 11 Jan 2024 04:58:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 05:02:27 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 11 Jan 2024 05:02:27 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 05:02:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 11 Jan 2024 05:02:46 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 11 Jan 2024 05:02:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7fbe5aa6b4fe7cefda24d4cc70b9d7345aa6d93be5fe42f5f6c5e49702b33a7`  
		Last Modified: Thu, 11 Jan 2024 05:17:59 GMT  
		Size: 145.3 MB (145266341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5770f04b332219aa9916f8a115635f86aa06b14c9d1842d01489e148d6c6a79d`  
		Last Modified: Thu, 11 Jan 2024 05:20:02 GMT  
		Size: 69.1 MB (69062032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32049dad0c224fc796fd5b1440dfed8a511c6e08ef3029e7a3ffd4d56f08dab4`  
		Last Modified: Thu, 11 Jan 2024 05:19:54 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:36777b4f2292befbe2576fdf048c1ffa2b0b307d457e32e98f9d6e2d5a28bc6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (239976817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d37706c969d51941b1503fd7b04224bc3a2f882e0c859284bb0d77fd9ef64a1`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:11 GMT
ADD file:262fd7bf0bc26e5d2a229fba52626e22b8a93beac29733acfc60e716c26e689d in / 
# Tue, 19 Dec 2023 01:41:11 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:54:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 06:59:31 GMT
COPY dir:679954ac595f0d76b401a9a7d1ae039330e7231cb1c29892d5f56a0e84534783 in /opt/java/openjdk 
# Tue, 19 Dec 2023 06:59:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jan 2024 20:45:24 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 04 Jan 2024 20:45:25 GMT
WORKDIR /tmp
# Thu, 04 Jan 2024 20:45:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 04 Jan 2024 20:45:40 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 04 Jan 2024 20:45:41 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:24e221e92a36ab5b0075dd156b4f2ff095532a9b0927946cf6070bb1bea208b8`  
		Last Modified: Tue, 19 Dec 2023 01:44:38 GMT  
		Size: 29.2 MB (29157269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3caa98fe64b6e771f2487121c32bd24ed3c1efe0b70cd6eba73ff5a9db11b6`  
		Last Modified: Tue, 19 Dec 2023 07:16:03 GMT  
		Size: 142.0 MB (142001823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3932ffa2101c05c1f67077c33ccd734c0ac116a29b34bb25eee4421759d39c0`  
		Last Modified: Thu, 04 Jan 2024 20:55:41 GMT  
		Size: 68.8 MB (68817109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e58c6240636f1d8c1750d906cd60e6c104b81322e6f3bfd50a12795912172a6`  
		Last Modified: Thu, 04 Jan 2024 20:55:33 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
