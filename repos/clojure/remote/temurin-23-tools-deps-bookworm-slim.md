## `clojure:temurin-23-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:02fb5143117db7fc9e61d36259a7c53a419f051fa4353aa44abead5a57bb057f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:61e784f3e70909587e54b87f8135a56c6493b48f209391b34c42944c0e3bc2b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263066726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:930048f9dfb614d4ea08d3e7050037272768b53c727ebb6a03ccccbfdd10cdcc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c144a35df342cbdeced747028d12847c39845eb8c430279c798a2a997de05966`  
		Last Modified: Tue, 25 Feb 2025 02:35:55 GMT  
		Size: 165.3 MB (165316182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1f07e82c82561294eb2fb2ca995abe60428e9a56ea4aab188bd61e553aaf80`  
		Last Modified: Tue, 25 Feb 2025 02:35:51 GMT  
		Size: 69.5 MB (69530202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d79478f9606f198bd1b4c7ce071ee9a71a2b0fd09f66a6113fcfb6dc8fdcf8`  
		Last Modified: Tue, 25 Feb 2025 02:35:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad39fda5a689241e98dccc4b0e57f80b4dc8d02fcfb965a6762329626137e1d`  
		Last Modified: Tue, 25 Feb 2025 02:35:49 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7b358dfee3614c67c93f4b13a017dbe73ebadfe7dbf55cb6b2e60ebfb74299c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4933468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a09467a2356ed2f719c7f7e96db4836e6a0f83dad80e5202b326cbd0a50dd6`

```dockerfile
```

-	Layers:
	-	`sha256:d5a0760d018e53f56a187475fd574dbd330f450e90acb2036de5b6642234bfed`  
		Last Modified: Tue, 25 Feb 2025 02:35:50 GMT  
		Size: 4.9 MB (4917590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20fe3101cb1cf242f5d84e2ba03b4ea9787f4eb4f713591e294a36b014a67beb`  
		Last Modified: Tue, 25 Feb 2025 02:35:49 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7757195d838fd3f76a2d4e7755a9f0ffe158410f635c429aa7061f0d315e5fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.8 MB (260770065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f76eecd2fd62fc43f7bf242b7d268ef54d15d5a78317aba049e273202de86aee`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30e270119480fbefdf8c02be71a5c10e0152c3fbecd3e1dcbc4fae3c4f0badd`  
		Last Modified: Tue, 25 Feb 2025 11:16:10 GMT  
		Size: 163.3 MB (163341441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3bdde2f045bd09f9f115d6f2d4953cf6f895880ba8c7400331f5d5682dcb85`  
		Last Modified: Tue, 25 Feb 2025 11:19:40 GMT  
		Size: 69.4 MB (69379159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f06df16d429c3b64088344257179331ad2687ad8f2980dac79f32bf6b0a56a8`  
		Last Modified: Tue, 25 Feb 2025 11:19:36 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97de34cf31628d8fc3bbe81a45a33cdeaa85e8d627bc58b693aa7bf0b7482b76`  
		Last Modified: Tue, 25 Feb 2025 11:19:36 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:89c93afc09f3773f6fae3f310f3d04605aec19e7f089a79eb2d06ca815e657fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4938726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5908a9d11bd8e70f913be24133b248875039da5522207d91a0ca525057d36d`

```dockerfile
```

-	Layers:
	-	`sha256:de90f68b6604a93efe0f26cadfde609acc3c104c14a6d9436bbcf529dfaaea41`  
		Last Modified: Tue, 25 Feb 2025 11:19:37 GMT  
		Size: 4.9 MB (4922730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:756c27750593488486981c0e4df2a198e82e675369c179c2707cdcb7bd5feaf2`  
		Last Modified: Tue, 25 Feb 2025 11:19:36 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
