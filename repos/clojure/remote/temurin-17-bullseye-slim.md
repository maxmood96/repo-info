## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:7631acdee855b7ac0676594666c43d64eee8eb20c6b157cdd27dc5bfc63127bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:cfb8b6bf563e0ef9c7f1cfb8ad96caa489b5fd9041a2b38e81f9ff7496de5fcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233578205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb1c3db54122e92c7346969d4cab7f5086667ec4900e9a23ec88c5f73c0e82a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3491c374b8855ec5debf98a07bb4889ca169d746c85dae1b541f6e1bdcac23`  
		Last Modified: Wed, 29 Jan 2025 20:27:38 GMT  
		Size: 144.5 MB (144536692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a10f37977b3383bcc9d7236572d80ed8473f8f1b02d0fd8073181875b457b0`  
		Last Modified: Wed, 29 Jan 2025 20:27:36 GMT  
		Size: 58.8 MB (58787810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ea964f9cb9afaf9d59aa4d79943bb64464bc57c66a7a27f737c5a59c0350a1`  
		Last Modified: Wed, 29 Jan 2025 20:27:35 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3faf2654ff79652409065e585119fb194c3ad88d67a749a67f63b91bb989a6b`  
		Last Modified: Wed, 29 Jan 2025 20:27:35 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4e806e6039f99fa99ce60a7450a450fcc8c29bc10d9feb83a2d314dff43c6eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe83e48f09bdedb94de4af4f1db9cdc8185bff1b09992ad413505f979bb47e58`

```dockerfile
```

-	Layers:
	-	`sha256:0b4677d6fc4d8d8e1af0af1c3fd682f6dc0a13b4e00269bd85f2ee534d702dbd`  
		Last Modified: Wed, 29 Jan 2025 20:27:35 GMT  
		Size: 5.1 MB (5117069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a4bf33e070b05272c0ab1d4497f6f4725dd79c29079e775b616e80c91a4328f`  
		Last Modified: Wed, 29 Jan 2025 20:27:35 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5e35327b38280f6a2a9141bb63067a3467253bfc81ef19c94c3adc5fe005d954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231016077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90b1c1560e6af104bc84d715f44a98682c7b03b8472999e7a070d755fafc224f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8046fc472af52cbd0c18bb2ee9a2dba25212fe858739c56750d18c3352f2396f`  
		Last Modified: Thu, 23 Jan 2025 00:48:42 GMT  
		Size: 143.4 MB (143360974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe4819ee267bdff0940d2577c922f82a809399b6e95cdc55d29b21b1a0c6804`  
		Last Modified: Wed, 29 Jan 2025 20:50:29 GMT  
		Size: 58.9 MB (58909148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88bfa6a35ee045d26f8907a475db268c5be03df08eff651c33c4a7e9d308bdbf`  
		Last Modified: Wed, 29 Jan 2025 20:50:27 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ed9b87b41adad1563de23a9e0b4619ec607a816a10de4aa4b6e131f326aeca`  
		Last Modified: Wed, 29 Jan 2025 20:50:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:67a56bd04bd26ebfaeda0acdb660e20e00d35e534a59c4119761979d45f14710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81367a1caa35f764193d01547dacdd6e2183790bc98f99c76ccef6099e73a25c`

```dockerfile
```

-	Layers:
	-	`sha256:31cf94ed948229d9cf89fb9bc757b4e04c4f95f9e3a72dc2473fe188da0142de`  
		Last Modified: Wed, 29 Jan 2025 20:50:28 GMT  
		Size: 5.1 MB (5122801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b5a286ae65e1902f80df4eb801463683593003759075f8e0230f8efa92e8e14`  
		Last Modified: Wed, 29 Jan 2025 20:50:27 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
