## `clojure:temurin-22-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:11a7a84b8a4628c50abc12102916bbcf5486dd9681f61c24e6fdc5bcd6ce463d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:a62a2170cc573cb3d32c2875550f1bf0e6d5ee103ec974d9a0d02e176bd363c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.8 MB (286784754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c729b20876de3ff55dac80d03f4cd603fe6af4927818e27aebe9e6716b31e59c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ca994ce711f660090f8c9c14d9b14d6b5740ffe0739f7fd73d4ec693a12988`  
		Last Modified: Tue, 23 Jul 2024 07:14:18 GMT  
		Size: 156.7 MB (156715517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857a5d682765d318881d697560e56befe91276b7b4b09118eac488c077b73e4e`  
		Last Modified: Tue, 23 Jul 2024 07:14:21 GMT  
		Size: 80.5 MB (80514122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a40c228088b57c01e3e55e41aaa5e2bc8452a5f1a70b6de7c22f886d43eba52`  
		Last Modified: Tue, 23 Jul 2024 07:14:20 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad6b3b945a93a5b46a130156c74633549e1dc561255ef15c5a3dcd79fbb0fcd`  
		Last Modified: Tue, 23 Jul 2024 07:14:20 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:af25ba55625b0ebce5b16dc9ecfe6481f888c37ee5943bfc2261300f8d55d480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7016887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439765d1a5edd72971dd017561d6188ce9c66a1fdf543060d962a03c88f133b2`

```dockerfile
```

-	Layers:
	-	`sha256:51ae15c045fd8eb0a483f411d85f85b3fe47d611e63435a3518113c419d58aff`  
		Last Modified: Tue, 23 Jul 2024 07:14:20 GMT  
		Size: 7.0 MB (7000764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3080be4b7282e34dad4ed40460b2b32959c95d81ad569ce60f2d7ae616e8c5f1`  
		Last Modified: Tue, 23 Jul 2024 07:14:20 GMT  
		Size: 16.1 KB (16123 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:23c55647eb01fb23035cb22d9d8c827a275ae563ed92ee3586326233187555b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 MB (284586561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7203b01a3f6e750b4ac971bb13fafe4105aa8f1da5d92ff4fcbad7618bc08064`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8acbf8875a3006cfaadae4b6eed30ac6fbc216de012d0b8f7d79cef38eeb4ece`  
		Last Modified: Tue, 23 Jul 2024 12:53:51 GMT  
		Size: 154.7 MB (154738009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fa06566e68de1f649bfdf5a0f201fea59f11bf8d7c67ac462a7ece52091c9e`  
		Last Modified: Tue, 23 Jul 2024 12:58:40 GMT  
		Size: 80.3 MB (80259070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b848eced05bd8b749a42a3f1af76180ed810bbfe925728e59ea8a33e94cf94`  
		Last Modified: Tue, 23 Jul 2024 12:58:38 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c46fefe3ef0499abec547ac8c1a46c5bd8b8314a1db2351b8dd423c9c9abcd6`  
		Last Modified: Tue, 23 Jul 2024 12:58:38 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c786445bc6818774c812fff960c688e2db2f1841951c1dd9ab2b1391918d146f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7023858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bad0c305cb5a59ed06676c0b25ac2b2e159b318a4c8605fbb1707c9e9c77036d`

```dockerfile
```

-	Layers:
	-	`sha256:0c1a503ec63f901df9d2aa885c7e3a397fc67361fa52f1c0c78b4283cb435c47`  
		Last Modified: Tue, 23 Jul 2024 12:58:38 GMT  
		Size: 7.0 MB (7007175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bb851910b507165403fc08aa1af8cca9934b677f1495bca5802c22e9f92c10e`  
		Last Modified: Tue, 23 Jul 2024 12:58:38 GMT  
		Size: 16.7 KB (16683 bytes)  
		MIME: application/vnd.in-toto+json
