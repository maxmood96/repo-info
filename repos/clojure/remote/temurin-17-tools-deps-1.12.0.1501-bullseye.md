## `clojure:temurin-17-tools-deps-1.12.0.1501-bullseye`

```console
$ docker pull clojure@sha256:9edb1a0823c397c7b2b420cd5ba499ded65da0a3de22d87a7a881fecb8fc05ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1501-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:c939488246c6e8239e5458da49c095495f00e8470507418d168c8f51e5a88ab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.5 MB (267497819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48ca32a1f8c6b59da8795731b76a2f6cdca7f1e034c677bcc9f649da562e1ec4`
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
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c27acf368d4c488f02189f0f3bfd60f53b48d9cf6834acbd5a1e8d53b011d4`  
		Last Modified: Fri, 31 Jan 2025 02:17:56 GMT  
		Size: 144.6 MB (144566500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748687608631506b4d3b8d86b6f3135b6d1598c28c28b83e2949de7053c7f17c`  
		Last Modified: Fri, 31 Jan 2025 02:17:54 GMT  
		Size: 69.2 MB (69191113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8eb52a43908a92b5c76d08e5a128a8c1cb0dca0971e544eb0e83ebf23e2047`  
		Last Modified: Fri, 31 Jan 2025 02:17:53 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13c92570166116020c93347e45005849e9950c9aea60bcc5aa417d1abf637ce`  
		Last Modified: Fri, 31 Jan 2025 02:17:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1501-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:91f5c8c78a1776e9586aeccbce03ca0fb8b47f4c57dcca3b2a079832fdcbca00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7220375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266b74fbb271a74c316ea5098227e294b54a65065b080d9e3072561c21477938`

```dockerfile
```

-	Layers:
	-	`sha256:ca779f47843a8943f836b94934cf972acaa73fd5e4b26e4b21dca5d103c79bdb`  
		Last Modified: Fri, 31 Jan 2025 02:17:53 GMT  
		Size: 7.2 MB (7204555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d78e2280374fccd70b41bcf10083be49140f9576dbda2d0af2b6afe4cb984dd3`  
		Last Modified: Fri, 31 Jan 2025 02:17:53 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1501-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:17a248372c6ac8b4cb4a8a473c9e9ae7eddf3880ad2c0bcd9ac54b9ecbc72e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.9 MB (264918950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e31705393861168daa8e0d8d9de3bcd130ed4a57432ac7e04e3b693f6561beaa`
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
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a83cadea50845dd03abea7a3d6efb27e951eb9e87f1d5e10c0e89572e38b27`  
		Last Modified: Thu, 23 Jan 2025 02:46:21 GMT  
		Size: 143.4 MB (143360991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c269e18cbcc7c6f5a22d051b05f8155ff89382f6ac7efe1dc7cfcd23f90a59`  
		Last Modified: Wed, 29 Jan 2025 20:49:41 GMT  
		Size: 69.3 MB (69310859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12b876c5b234b955ab34a2e7c6c1ddc8920cb235b94910d302ea013c25df299`  
		Last Modified: Wed, 29 Jan 2025 20:49:38 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6c88368c6b30bb6a150e930e3097a10c9ad5d2f190aa79a6e120084c9fb9b8`  
		Last Modified: Wed, 29 Jan 2025 20:49:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1501-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2ce8b20ef16c328be4211fd85949b933cc6db3e7179c9d0fd98a0f7bd677cb2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7225595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea0ebddd6cfebe99b1f395529f9a5e6bd3fba8d8de43ada6eac8609f68bee50`

```dockerfile
```

-	Layers:
	-	`sha256:22bb2d7e26a442e58aea62cd7049a3b7610da8298d876fd8d5a2b2d648c0fed2`  
		Last Modified: Wed, 29 Jan 2025 20:49:39 GMT  
		Size: 7.2 MB (7209656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99a1e498034457f666e3175a2a7163a360a78d68898ee281e272d9cccf7e42b6`  
		Last Modified: Wed, 29 Jan 2025 20:49:38 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
