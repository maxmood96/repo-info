## `clojure:temurin-23-bookworm`

```console
$ docker pull clojure@sha256:26bbf1d12d768b591a93eed77e71c817abf5ac5dd5da75feb8120f1ab02429e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:8165847fb15729b15b3ef18d9a4764194d8b17872e01e3e4e35f64dc53a22c95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294754129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:241634231b3fd6069caaf235288190c5a56ef2650153360180198f9cdd05a6cf`
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
	-	`sha256:9d28fd6b84cfc70c68d96a9b46dc89d01b286afa28d3d77b93f863652142d22f`  
		Last Modified: Wed, 22 Jan 2025 19:42:34 GMT  
		Size: 165.3 MB (165295134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4890fdaed54e8a94576856dd22f91b9540313265af9838380d715d7d96f672`  
		Last Modified: Wed, 22 Jan 2025 19:42:33 GMT  
		Size: 81.0 MB (80977989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5153e344e9d69c88433d1449f7d6171fff2bfdf8a44e08c5a3b3c11bd07015bc`  
		Last Modified: Wed, 22 Jan 2025 19:42:32 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c948e6b543921be6ccd5c4d180ba917026fe3cc184abf3a1f1cfd7aff50c84b`  
		Last Modified: Wed, 22 Jan 2025 19:42:32 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:65690afb4e5b3e4a1f90dc1d9b1c91ea048289a30d932267fe01e63c02f652fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7193273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e3a793b47d0e6b9c58695f4dab5fc11d1f9b8a065eaae0328d84d7eff04330c`

```dockerfile
```

-	Layers:
	-	`sha256:4ca1914e8628cd7145301aa456f2e4e2cb38c07bf4c1f406ae03c59434d8f11a`  
		Last Modified: Wed, 22 Jan 2025 19:42:32 GMT  
		Size: 7.2 MB (7176769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a82a4dab03b58954b95fc62f9de43be7ee73301f60aeccd906036c78eb02d3a4`  
		Last Modified: Wed, 22 Jan 2025 19:42:32 GMT  
		Size: 16.5 KB (16504 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1ca600554ae5762561477f7f89ce924968a32412352e5ef579f5439f72432fc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.4 MB (292415706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d4d75af90602f66c00acfc551fdbaf5cb2c9b96c3d56a40a074ff84920218e9`
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
	-	`sha256:eebbf68effac48458d835fb306b89c32b356ec1a36dac9070e972dcdaa0c8dfc`  
		Last Modified: Thu, 23 Jan 2025 03:53:51 GMT  
		Size: 163.3 MB (163281805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680579765eb9af99306134ff394d459dcace58a523a4a778a3f05881387cc1ec`  
		Last Modified: Thu, 23 Jan 2025 03:58:28 GMT  
		Size: 80.8 MB (80825966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eaced769e4cb546d6dd4fc86945f163fadcef9fbd8692aa10e1ad6ad12c75d5`  
		Last Modified: Thu, 23 Jan 2025 03:58:25 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caeb00fc07e45ffd60d2cdd42bedd10576cc99e8ed6293815e75ff536f3862c6`  
		Last Modified: Thu, 23 Jan 2025 03:58:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c9020023b2711bfdfcd79b8b4ecafd7a7894c3cbe7607ddcf22fefd6f4a813cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7198581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe24c0d04106d7ede9c638cb920cf2a29bf1f3ee094e3dd125536873e491cce2`

```dockerfile
```

-	Layers:
	-	`sha256:bc6f0c539584065e5503d31313bf9a2be480899d2648de351317d47fa7de581d`  
		Last Modified: Thu, 23 Jan 2025 03:58:27 GMT  
		Size: 7.2 MB (7181935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d32ab4eafdd76df3d6ebd6692ff5dfddc6d33e4c3d21571c9fb828575d7f1e6`  
		Last Modified: Thu, 23 Jan 2025 03:58:25 GMT  
		Size: 16.6 KB (16646 bytes)  
		MIME: application/vnd.in-toto+json
