## `clojure:temurin-24-bookworm-slim`

```console
$ docker pull clojure@sha256:b66f414e4aabe8ec2a3267de3a1e9b52b3f012ac5530be56ccce022ddb864515
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d26c8ad75d31ecb462ddfc1b7c48d9afa84cb6b2861a123185a072789354521f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187706435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a846a6d06ecf0f3b235153605265a613aa87d133300472b83d7445cd2b49b271`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9422688b73396143d24133eac30773a2e9e6f4d221585795e30d37d25fbf1ee`  
		Last Modified: Mon, 28 Apr 2025 22:08:12 GMT  
		Size: 90.0 MB (89951979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb1e627f61c513f67fb2de5651a22602f2773ea00d0bc02ad7c2d017b842e3b`  
		Last Modified: Mon, 28 Apr 2025 22:08:12 GMT  
		Size: 69.5 MB (69525777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3bef49c7acdb6cce5ea5ea312d4d0cd0495ce9b207020a32e0e63f5e1460d33`  
		Last Modified: Mon, 28 Apr 2025 22:08:11 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefd71d4293a37ebbf0dcdfb8ee78c2ef7a53bc28d66265e95d383c74932f7c2`  
		Last Modified: Mon, 28 Apr 2025 22:08:11 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fb04a1bf4c506cd75df0c3c52ade650eeb9b92eea7d18099b53478f76db14714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4880482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4302935cf1b8be013b9068af72f2482744a2ee9437138ead9f4135ccd3ac92ea`

```dockerfile
```

-	Layers:
	-	`sha256:163e8ab1ce7dcd14d59961ba88ff4df7025cdb21dd6f1f211c049c64ca44fb35`  
		Last Modified: Mon, 28 Apr 2025 22:08:11 GMT  
		Size: 4.9 MB (4864611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3896cba406535dd0ed6fbd63668293a7f5ef2423ae043ce04696c6678bc571b3`  
		Last Modified: Mon, 28 Apr 2025 22:08:11 GMT  
		Size: 15.9 KB (15871 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:468a1ecfcbf430d50b616981d273d2f2cf17e7d57f6abcf0042f8bc9479c7e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188808108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24247742233d3d859fcdd8ba97921662fa34d631cda7af8ab1466ae47f0b1abe`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df648a39290a88f8540ed431a61c0008b1c7e9e4940da60be9b66334267a83e6`  
		Last Modified: Wed, 23 Apr 2025 20:03:44 GMT  
		Size: 89.1 MB (89091255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604800b5abe38f1e15898d0fade319a15d131b95bd75058cdc72136ff73b596a`  
		Last Modified: Wed, 23 Apr 2025 20:07:38 GMT  
		Size: 71.6 MB (71649488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee2b543267c675d957267e3d94193a3c7a2b9b5577affb6610faa706ddc8e3b`  
		Last Modified: Wed, 23 Apr 2025 20:07:36 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c983803606aea4f6a2e111c655fc0555ade883b10ec13d9c83408c8950f5af72`  
		Last Modified: Wed, 23 Apr 2025 20:07:36 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6747c3ba4132b41c24c2109d0b28713e36695d33a657795c44edcc74fa51f8a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4886359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77c03b974bd823c02a840acbe8fd55e87e2bf5fdbcdde7cacfa59ccc28741e5`

```dockerfile
```

-	Layers:
	-	`sha256:95a8919539ca45399b901fd570bd12d1822202fbf357e268053f8726fb3655db`  
		Last Modified: Wed, 23 Apr 2025 20:07:36 GMT  
		Size: 4.9 MB (4870369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62bbd74e913739b3e74a9aedebf4189bba2aed98600e3900be64c6df47e38a61`  
		Last Modified: Wed, 23 Apr 2025 20:07:36 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json
