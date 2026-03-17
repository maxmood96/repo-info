## `clojure:temurin-25-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:b65ddc934661e496753fd88fa48b4497f65a5307fdd3a686902108cb6f801978
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:d12f622a66d276f3687d6bc897b7adaeb51d4f6555f84033996de118f66518e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.6 MB (215607069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:334e993cb9664aee8b0f60571e3f9d00fe8d9eb298a1df48ef4c888b22eee5b8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 03:01:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:01:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:01:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:01:13 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:01:13 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:01:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:01:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:01:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:01:27 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:01:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e759575b5b0029fea51256b7ad3afa90c8ff1a6a9457787359c2b05b4a964edd`  
		Last Modified: Mon, 16 Mar 2026 21:52:53 GMT  
		Size: 53.8 MB (53762481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50166dcfd53a3a49c1834a353e4e6ce4b60a877e7bf7d2ec85f75f0146a1ef3c`  
		Last Modified: Tue, 17 Mar 2026 03:01:50 GMT  
		Size: 92.3 MB (92256289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238fd6013c0d061e70585cfcae661cd97a522158e056bacb86ea8ddc1d65cc12`  
		Last Modified: Tue, 17 Mar 2026 03:01:50 GMT  
		Size: 69.6 MB (69587259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c757656fa66b1dda5fac19acff40b7662121b71c89739fe82cd67155529a629`  
		Last Modified: Tue, 17 Mar 2026 03:01:46 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7da3de9a8537b9a6c3e59413826dd3fd64eb1ce47f34fad026bdafaa88c4256`  
		Last Modified: Tue, 17 Mar 2026 03:01:47 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7bd08dd172fbf291116e658bc2ae1eba24e57671d3242c47bbdb7588d02681da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7392174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:644ad9ec7fa66f6eeef801ad0004ff121a4dbfad2fd33c0e74bdd2302b346387`

```dockerfile
```

-	Layers:
	-	`sha256:98c7abab7eaea89821a6ac828a7bbf094002b7712be3caee043887ae2e5bbea6`  
		Last Modified: Tue, 17 Mar 2026 03:01:47 GMT  
		Size: 7.4 MB (7375727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70d8fb545200af40673af77745b3c88ea235d899dd52dcaa7b77aee6eb96f894`  
		Last Modified: Tue, 17 Mar 2026 03:01:46 GMT  
		Size: 16.4 KB (16447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:32409578b60b05d4e362282017134d05093fdb1faf0b5112e48101eedc0aa123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.3 MB (213264846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7d18703a3720d2c4eff21f3b54ac37ca04d7c243fa81b209e9a5f782507ed4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 03:06:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:06:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:06:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:06:05 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:06:05 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:06:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:06:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:06:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:06:19 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:06:19 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:da8e260297fdb91b3f012b26dd982feb43d0bf977ff8adeb7a850ef9c5829770`  
		Last Modified: Mon, 16 Mar 2026 21:52:51 GMT  
		Size: 52.2 MB (52247254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21354101ca9267107aacb707f22ae6c57d6c6032cf97fa0e1d12bfbb029aba3f`  
		Last Modified: Tue, 17 Mar 2026 03:06:40 GMT  
		Size: 91.3 MB (91288272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a8e1f490b9cc1d7adc66f4a915f3b0d19fa00dea7fcff39ef0450ed391ccaf`  
		Last Modified: Tue, 17 Mar 2026 03:06:41 GMT  
		Size: 69.7 MB (69728280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:debc8e744e926b9119e47afb03abd93c8b91cd0bb96b12001bb813518508b5c0`  
		Last Modified: Tue, 17 Mar 2026 03:06:37 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e336e560303f26f5aef141624efe3ba06f5338491b117589eb07f538c1afe60f`  
		Last Modified: Tue, 17 Mar 2026 03:06:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:86c972ce0b0d03cdbdaa3e5a7857381a6ddb9f0b41a0907a2e672cd1c621e549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ec4a62e68f7401b16ea542bd8d71c933fef33d6f9b0f1d46ecb0d99badbd7d`

```dockerfile
```

-	Layers:
	-	`sha256:2aa47775e904ea29be6676cd5f5bfe615468c8399239bbc69624aa7d5540f9dd`  
		Last Modified: Tue, 17 Mar 2026 03:06:39 GMT  
		Size: 7.4 MB (7380847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca6177f3fde642a11bb58191da3c14a47cc05941bc83c9bf7dba15cf3cad4b70`  
		Last Modified: Tue, 17 Mar 2026 03:06:38 GMT  
		Size: 16.6 KB (16589 bytes)  
		MIME: application/vnd.in-toto+json
