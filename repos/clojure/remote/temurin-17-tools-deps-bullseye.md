## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:27d9753b7cef0e3056576c0dab02150276ac7c4b3f3a6a061c7c52b3aa2272e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:9926f306a9aa27fc2573006fcf7ad6c45c38d1cd4642246a61bc9ad38a3921d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268989391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88ed2618db6aa88b210716862b57d424c1d05d5d49d3b41bb62d982af3c13de`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:18:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:18:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:18:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:18:51 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:18:51 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:19:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:19:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:19:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:19:05 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:19:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e3995869c0472c9d0bacb5715e2e1e1625b4c1ea5d526ca8ad011132490029`  
		Last Modified: Wed, 22 Apr 2026 02:19:29 GMT  
		Size: 145.6 MB (145628761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ba3bcf573e5a4e7a350a4bae501929b0855c31a3f86f931e0a0bd6ddd13e3d`  
		Last Modified: Wed, 22 Apr 2026 02:19:28 GMT  
		Size: 69.6 MB (69596437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e952ebeb30b26d95f0e6b841f7612521a30db1fcd1382d4383fde3ce31da9e56`  
		Last Modified: Wed, 22 Apr 2026 02:19:25 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d265c7a21733dc938da6a2a8f7985e8a413f7b22f3fb3dcbbc65b094b5a0f0`  
		Last Modified: Wed, 22 Apr 2026 02:19:25 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:46103aa04aeac93cf7040e8e7dc4831f335fdfc72ae78e10783cd8f4264be2ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7423431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54cc0b070972019fb6b254ec75774e0c00e368a26bc0b593c608b9490956f65d`

```dockerfile
```

-	Layers:
	-	`sha256:7d6b74a8a9369cb6bb67fcb7d654bf31beb3e5d4852a3c24921ab4230780c6b2`  
		Last Modified: Wed, 22 Apr 2026 02:19:25 GMT  
		Size: 7.4 MB (7407653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b0ab28a58cf0d64183d27f25a515e3fa0ae806565a96a2fecfbe555f34eca31`  
		Last Modified: Wed, 22 Apr 2026 02:19:24 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:85993d8e46a0b12d3bee0e84e2067af8c37ec431fbc3446c6974989b7b4fcd1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266429120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35aa3da8332f63af763016605f851cd52108701cf57831ead0357b15c65376fa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:21:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:21:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:21:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:21:46 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:21:46 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:22:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:22:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:22:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:22:00 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:22:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b230b0d27d25995ce35ce99ec1878a7e64c7f28efffac96ae27ae0d1df671f8`  
		Last Modified: Wed, 22 Apr 2026 02:22:23 GMT  
		Size: 144.4 MB (144436187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf11a66daaf2a9bd678319fa3869db51dfa3a0e04d7e8209324118b8ec1bb799`  
		Last Modified: Wed, 22 Apr 2026 02:22:22 GMT  
		Size: 69.7 MB (69738891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38e3b2753aba4a907ec4d724c77822049664c9e5b200e319bac46852480a09c`  
		Last Modified: Wed, 22 Apr 2026 02:22:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e529dc747a4bfab16a3f735563b3cf3452f6b85c3acf40cf4dc40f7c7b8347`  
		Last Modified: Wed, 22 Apr 2026 02:22:19 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a6105a992c6da9f321bd3cfd6cbbc8476da85b3c8ceea500fc31624c6e4094ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7428648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a24d980ea92d79c7bd9de930524b254daa0745ee169d71592a3b3cd0e2aaa47`

```dockerfile
```

-	Layers:
	-	`sha256:533b45005c3b7cdc37ebcfc17654f18e2d19aab537677d06cabc5c515b6d1edd`  
		Last Modified: Wed, 22 Apr 2026 02:22:20 GMT  
		Size: 7.4 MB (7412752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9216ff1cab42521e60a79331b3cb07f005c49823e7fb2add6bde52f31fb563d0`  
		Last Modified: Wed, 22 Apr 2026 02:22:19 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json
