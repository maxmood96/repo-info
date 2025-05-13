## `clojure:temurin-24-trixie-slim`

```console
$ docker pull clojure@sha256:a9aefa0bba340b979c0e188808e679cd6f97ddce5344d3921a1e9f67c980f173
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:daa953f5ba697b93a383213af841e1e7367fbffc7265d2cb591f595419518cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191430988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4503ce2d6ea51c154df3ce013c62effa542c077d07e079d46438fd4fc75ddb10`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3ae34fc80ed56f2b3a9a0b682b58e28e57fe981f5e514c3f687044f4b967608f`  
		Last Modified: Mon, 28 Apr 2025 21:08:25 GMT  
		Size: 29.8 MB (29753912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543a4cc9777670296712f6a9872398e4d4ea99fbbc7cd6c8fc0c4b43902d72ce`  
		Last Modified: Tue, 13 May 2025 17:53:57 GMT  
		Size: 90.0 MB (89952000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee2cb3f7f9d8ca4965002f2b869a674e825f883763d550bc2f0f5ec0d40a6cc`  
		Last Modified: Tue, 13 May 2025 17:53:58 GMT  
		Size: 71.7 MB (71724037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81f8a5667643cd7ea85b65caff56ee1803a9ab0df3ec8eabf041e825b2f5c2a`  
		Last Modified: Tue, 13 May 2025 17:53:55 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd344e9802cca5f089023d85ee1628a25d18e6803d73acd7efc8e4b6530a6c6c`  
		Last Modified: Tue, 13 May 2025 17:53:55 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:02c7857900867b63b57dc20a6a2807e68a95b113ba63482b3209825449316689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5033181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c59433a590b2b0d5c6d9997077cb57f13c9057d161c6406da5c21a5132fdaeba`

```dockerfile
```

-	Layers:
	-	`sha256:098d006171614f80d837a7b2cf6084cf0491aadeef5f6edde624611f10d57e57`  
		Last Modified: Tue, 13 May 2025 17:53:55 GMT  
		Size: 5.0 MB (5017333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b2a218b63474ed7f5e09aa661da929ad97a99046dc626c9f6131b904f91de1f`  
		Last Modified: Tue, 13 May 2025 17:53:55 GMT  
		Size: 15.8 KB (15848 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bc452bdfffec80a52570be4c3fc9f1066703d507a20a5e5579fcef6929120d27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.9 MB (190868809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e6c0133162ff11b2f528d7e50afe0dbe0daa431813c956c8657d6c59897cf9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d0342bfffaba1a8be0950e44b5334c6cf9a05d9eedd81a042ec7813ac91850a4`  
		Last Modified: Mon, 28 Apr 2025 21:23:36 GMT  
		Size: 30.1 MB (30130233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf78d6205bb385dbaea21715ebe2773e6352d0ca5870bdfcb0e246524d354c9f`  
		Last Modified: Tue, 13 May 2025 18:09:24 GMT  
		Size: 89.1 MB (89091185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b82f5ff77071957a46ad0bbf072d8fc45c22d89872e04cf749ee5345d7cf2b1`  
		Last Modified: Tue, 13 May 2025 18:11:31 GMT  
		Size: 71.6 MB (71646356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c528f3ac11805a1dd5769746be59e1b69c1fd644e634814b8d88cddbb1703eb`  
		Last Modified: Tue, 13 May 2025 18:11:28 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e8b0e9b65ab1ef53701ec31c7eebf3b364fb8884a2a65eb51070734fb44ee5`  
		Last Modified: Tue, 13 May 2025 18:11:28 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:741f432648c64ea962929480e17378fc938b9abc9ce2c51405cf47d6b4231520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5039064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c326b0ef865df419347b5770ede22b21820c79504cefed3e6ccc951be95acb4c`

```dockerfile
```

-	Layers:
	-	`sha256:5cef5ffdb4fe16bfa3603415d9d145d19b7600ba1eac195c9074876e8fbedd8c`  
		Last Modified: Tue, 13 May 2025 18:11:29 GMT  
		Size: 5.0 MB (5023099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05e001abd2d850fda1f5eb776b9e9280d05702ddbafdd7d17b0542f055848c4c`  
		Last Modified: Tue, 13 May 2025 18:11:28 GMT  
		Size: 16.0 KB (15965 bytes)  
		MIME: application/vnd.in-toto+json
