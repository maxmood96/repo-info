## `clojure:temurin-21-bookworm-slim`

```console
$ docker pull clojure@sha256:13ecf7b3c080b27a0e443af5e3b6887d882bc5bb230c572d367f21a169223bd6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e4062db96cfb0b5a4c87ab43d3d1aa3132a194ca4b620d6b6fb6112e638c8c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256178698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d92c03451bf9934c49f096c4c5246b604ccad3f3ff14b15257be3be9c55dc4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df8f519d0965fffacf4c8abd345fe7b9f455209c4cefc08803c6bdc1f2ce767`  
		Last Modified: Thu, 24 Oct 2024 02:56:06 GMT  
		Size: 157.6 MB (157568685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa091620b0858e13ac536a46d37eb63b662122250efa94418abd9abcb421b37`  
		Last Modified: Thu, 24 Oct 2024 02:56:03 GMT  
		Size: 69.5 MB (69482684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a056e3481b0da1b2a9bf374360f225ccb5f90308e083c529d2f9ed9a41788ae0`  
		Last Modified: Thu, 24 Oct 2024 02:56:01 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15fef7d5e9769f9704bd5385c0c14d431aa8cbef8b9ab3b3ba5b9caee56ecb5`  
		Last Modified: Thu, 24 Oct 2024 02:56:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:448fb932e08a47bdc85dd094b299538c740c3ea724f59ca41829f93c6ed468ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4940774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16135d0347f901b25bc80fac6bfab09508b0083e3c48d180a97f94edb592003`

```dockerfile
```

-	Layers:
	-	`sha256:06da7aab4b33c22c53daa376eddcd4fe544e0b3ebda277e49522f1eb90943132`  
		Last Modified: Thu, 24 Oct 2024 02:56:02 GMT  
		Size: 4.9 MB (4924395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3668748543cd222b32d63ab8fca80e0410f6cca847c35c3a31f1beed97a29297`  
		Last Modified: Thu, 24 Oct 2024 02:56:01 GMT  
		Size: 16.4 KB (16379 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f64b1ed7cb7e487b00db6b78b655333008caad54038f63786b870fe5f4a07688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254295554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af30f3490e1f552b268d529ddf722798dfa085aa0bf75c76a7923ce20f8b4fdc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31de618d5329242a89cabf67cd0c3841b6c256ef62dc7074f5494636b182a3b`  
		Last Modified: Thu, 24 Oct 2024 09:25:25 GMT  
		Size: 155.8 MB (155793069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182f699111b18617ca5e05ba1f2f853196600fd23649d82e1b1036ef9d80cd65`  
		Last Modified: Thu, 24 Oct 2024 09:31:34 GMT  
		Size: 69.3 MB (69345105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b4aba3c403838e8175e5038580a8ca16ca5ade96ed0a384768c7ecea069af7`  
		Last Modified: Thu, 24 Oct 2024 09:31:32 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7e8b2dbc3a7241a765ef2339304829cc758bfbb8692ecad6872a2e0b21cfc8`  
		Last Modified: Thu, 24 Oct 2024 09:31:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:467d4438ad736dc1fa7c3aedca343f9ccd07ffe5f91d1d6c349077eb6ba969b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4946736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec89aef540622c9b160942cfa98f8935dc09c694fc659b8de1b01c03cf1ba3d`

```dockerfile
```

-	Layers:
	-	`sha256:7a31a0370d6c990833fa8ed0b879a2740441c2c7a7857324ed1205d2b9026b07`  
		Last Modified: Thu, 24 Oct 2024 09:31:32 GMT  
		Size: 4.9 MB (4930185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbf8008722d358d1803b7a516afa4958ba082dc03cc9c98fe89f0c4c94d85b62`  
		Last Modified: Thu, 24 Oct 2024 09:31:32 GMT  
		Size: 16.6 KB (16551 bytes)  
		MIME: application/vnd.in-toto+json
