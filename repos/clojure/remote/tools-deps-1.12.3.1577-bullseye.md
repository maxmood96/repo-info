## `clojure:tools-deps-1.12.3.1577-bullseye`

```console
$ docker pull clojure@sha256:fc6d262d80f48aab94d88658ca8c0e3b5b9bf4d727146e3255eeb9452bafc5ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.3.1577-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:5070fb22162bd274aef3719486280322041b495eec5700ce5a595fd948b3c610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215363927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1da29b65fd809ab45c3cfcb348fb12b2bc86deca3501a932381a24cd7eb78e10`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Sat, 08 Nov 2025 18:46:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:46:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:46:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:46:00 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:46:00 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:46:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:46:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:46:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:46:14 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:46:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3231ac4979f112f860b0844d831780ad860b7b2a9aaacc913425d9ce68987f7f`  
		Last Modified: Sat, 08 Nov 2025 18:47:09 GMT  
		Size: 92.0 MB (92045301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ce345c52e0ccdcaae4fcb79255ada68b3244022854fbfb14a92d30bbb5917b`  
		Last Modified: Sat, 08 Nov 2025 18:46:52 GMT  
		Size: 69.6 MB (69560890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e89fd948864ee5152a985d60b6756dbcf70a03f4d341a6d00fb70c6768ba02`  
		Last Modified: Sat, 08 Nov 2025 18:46:46 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f096ed7a58f29f9c98a3d609645de4c9fe2c81467b315401bc47d1194d4d1d8`  
		Last Modified: Sat, 08 Nov 2025 18:46:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e727e4c18389f9b3e46548487507c2469e187c2c09f3512cd5c5e2136f95b763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7363454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13fb968bf22a254d0b2450c11c2e8acc661c540e7d1bd661de5f145e013d993`

```dockerfile
```

-	Layers:
	-	`sha256:fce0744925cee50ceb65c9a386b44b9eae170a8cac28e1164f9d95dea2deabfa`  
		Last Modified: Sat, 08 Nov 2025 22:51:19 GMT  
		Size: 7.3 MB (7347007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb3cb64e7e8cb4e25a7956ad6f66d5151ad17bcde3a84e9c2e3aca4d4c15e6b4`  
		Last Modified: Sat, 08 Nov 2025 22:51:20 GMT  
		Size: 16.4 KB (16447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.3.1577-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:25f86623d4e11ed00c315c86257714286d275f0d9e924ac4a2e9b0646a5817e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.0 MB (212999904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfdc0ee7d4e735f623a4c7411162b3eb8661042f6f80516401dba2fe08eb2e0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Sat, 08 Nov 2025 18:45:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:45:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:45:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:45:44 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:45:44 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:45:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:45:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:45:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:45:57 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:45:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfbcbc7b509bf0ecbeed57138f4131fd53b82f2e100c24d267c3ff9050d7442`  
		Last Modified: Sat, 08 Nov 2025 19:56:07 GMT  
		Size: 91.1 MB (91052503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff80785714e75b1a84cacf5d13b78b1b5d506fb1c926b2b73d9790a00e238fa`  
		Last Modified: Sat, 08 Nov 2025 19:56:08 GMT  
		Size: 69.7 MB (69688389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43e6eefd8919e9bbfa47f1c1956c207b23c81fb21b4bdf9ff26cdd668514067`  
		Last Modified: Sat, 08 Nov 2025 19:07:05 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6517a9bcf6f5791067d085a08074bd3f1f1c8bdfc0e5a94269264dfec89057e4`  
		Last Modified: Sat, 08 Nov 2025 19:07:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:95a76e7ea54fee91bddd468d42be766b080dafa1303e6552ed03062be63fdca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7368716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa8a2a7d8e008934f9e9632a61c1387a36753486eb4ce48cb9e8ae8e4d9eeb14`

```dockerfile
```

-	Layers:
	-	`sha256:1608c3b946ed357b97a407f555599abce2e7c2209b4e78666605c174c939588b`  
		Last Modified: Sat, 08 Nov 2025 22:51:26 GMT  
		Size: 7.4 MB (7352127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6d91bba50683fab420bef283417761004eefd77ae01fbbf0339c4d07de59a6b`  
		Last Modified: Sat, 08 Nov 2025 22:51:47 GMT  
		Size: 16.6 KB (16589 bytes)  
		MIME: application/vnd.in-toto+json
