## `clojure:temurin-22-bookworm`

```console
$ docker pull clojure@sha256:f571ff49f9722eb05aad53b5d1e08458f436eb988e3023bea2ad28b8e7d02555
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:a747451aa31d4c605dd1350a62f112ed248b54395b1a6fcfd2dc991a53c9ea87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286550720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98d6b83baa8a409c567bbbe0412f2086584b50b7798130b9843981eba02842b9`
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
	-	`sha256:3553ca1371a3338a2eb9cb7b149c25ae4c0e11b9bb56ec7bc9de3ea53c824ce6`  
		Last Modified: Wed, 24 Jul 2024 03:04:43 GMT  
		Size: 156.5 MB (156481648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec63764a59d2678ff10d3e900624881252b97ceebb3a7dba825cef7c715b4e5`  
		Last Modified: Wed, 24 Jul 2024 03:04:42 GMT  
		Size: 80.5 MB (80513957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2edab1737aa1f1f4d60aaeedf8a59b7c091338c32e972a652f908d1afefc2635`  
		Last Modified: Wed, 24 Jul 2024 03:04:39 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b914b36dc3870ef397a20aca7fb7e7d123d435769ce886777c4a6460c8a04a`  
		Last Modified: Wed, 24 Jul 2024 03:04:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:30e79439a85ae743eaf05c4c5c044423b50178167c8961572ac5281695dbde12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7016888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f942aa225e8b381f5106661d28906cad574a3d9b85ff6b896d6e683a847960`

```dockerfile
```

-	Layers:
	-	`sha256:c934a48900b3838bca54a94a4101629cfe2b414e399ffae8582908686c4a1d6b`  
		Last Modified: Wed, 24 Jul 2024 03:04:39 GMT  
		Size: 7.0 MB (7000764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a82b59c2616f9bd0156e4ec2dd7fac98eadc3c1bd6ae9a18839e5dddeeef3f12`  
		Last Modified: Wed, 24 Jul 2024 03:04:39 GMT  
		Size: 16.1 KB (16124 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-bookworm` - linux; arm64 variant v8

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

### `clojure:temurin-22-bookworm` - unknown; unknown

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
