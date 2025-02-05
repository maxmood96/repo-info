## `clojure:temurin-21-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:bbfc410d3625a65a85ab31d77d1406a4e471566632c94fa0afb0cd3d868f0ecc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4d7374f5c6b26592f5e84c77125764e32a1a90c39059446271fa7762eef6b3ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 MB (255330282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc062e0c3838a1ed082b57cdbdccaea4f2eab827de80601b0d3a65514a4ffffd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f5defcd34342522f5d8961283ec8f0f12bfd845c282831c5e1d3b4ac3a8d83`  
		Last Modified: Tue, 04 Feb 2025 05:21:39 GMT  
		Size: 157.6 MB (157585921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae3c5189e59404afa9895479a00149052580c980b75504b149fe4e8c8871ba9`  
		Last Modified: Tue, 04 Feb 2025 05:21:37 GMT  
		Size: 69.5 MB (69531020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50af7b402f682a909cd6ff268491118b33be65eaa83b77d15c3ee1d7db718f8d`  
		Last Modified: Tue, 04 Feb 2025 05:21:35 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9563d06f42f6b359c55f6997d593315c1b4d7723509c0462ffd9cc751cdb2c`  
		Last Modified: Tue, 04 Feb 2025 05:21:35 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:09f76455cd8fe24a5605b1a2dae8988cff391e709d522314fc51e24c9ac754f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4932940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbc8a31f9ee3944fc45abe33261fa824dfa3763b952b0bba7e68d3937b18a2d`

```dockerfile
```

-	Layers:
	-	`sha256:d4bc79a65eefb6a7c4fe86ddd6b65520889afa0ddaf5444c4c10077ec32e53b3`  
		Last Modified: Tue, 04 Feb 2025 05:21:35 GMT  
		Size: 4.9 MB (4916365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28dc0df58a2f6043c6fd72131502d9dc6dcd5ebd7cef03d98fcdf2565af5bed5`  
		Last Modified: Tue, 04 Feb 2025 05:21:35 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d72245383617b176d9a77c7db71fb8c3dcc3594fab0b513843425e6e95b7b9a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.3 MB (253282835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeee6cdcd455eb252bc5dbdeb2c87bfc0c58589052c5abfda11e3010967515ca`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7350927a264592e316264c7cd122bd538e575003045857f9e107bee0b62198`  
		Last Modified: Tue, 04 Feb 2025 23:52:12 GMT  
		Size: 155.9 MB (155859249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032fa444aa34916c8d0ac4025a42c9c258b33d37b74e3cc8371d8128e56f12b8`  
		Last Modified: Tue, 04 Feb 2025 23:56:58 GMT  
		Size: 69.4 MB (69381668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8ecb7865aacac20ec2fee6dbdbf32d2e19d8dfb62f7b502c5daf57f53828f8`  
		Last Modified: Tue, 04 Feb 2025 23:56:56 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56752fa0156f4da1243b6938a9c370d7b0ee2fa2b919f34884708c962bcd9b73`  
		Last Modified: Tue, 04 Feb 2025 23:56:56 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fbe08a65ac264ce49b9ffa229ec593672aed7fcabf7173a4349988b840c24c0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4938867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff2656187a1963ed36cb3d8f700c63f91e8b1e3717e482309e7071278e9432f`

```dockerfile
```

-	Layers:
	-	`sha256:1ab9a73b58cc076212e6d2ce3dcbe16d9aa0c6cf451ee1410f676285874c5832`  
		Last Modified: Tue, 04 Feb 2025 23:56:57 GMT  
		Size: 4.9 MB (4922150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37db734b5a2229d3a305caa396d720c9ae266d991a74a72ea901414ffdfd06a0`  
		Last Modified: Tue, 04 Feb 2025 23:56:56 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
