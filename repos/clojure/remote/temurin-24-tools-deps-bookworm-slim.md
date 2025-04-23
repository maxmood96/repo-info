## `clojure:temurin-24-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:4dc5fdadabe6890e285b6def2fbe3658a55b43ae0fb787921d76b55aa302afa6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6b4dee23c9bf2b046233cdb01f0aca47bfd8afe453adf7111a7b9d6252dae54b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190009996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6e4cced1c8aeb7778d21ae7af6ad873e8d47d31dc7971b3d5477129f7ae516f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9729e24309db641476bda2c8347775f8f87006c3455db8b57601597cc7b9c78a`  
		Last Modified: Wed, 23 Apr 2025 17:16:38 GMT  
		Size: 90.0 MB (89951970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd3becfe2cff5a924a964b4c43a1fe9cd4c4562a2674d6dfccbf27064c6298d`  
		Last Modified: Wed, 23 Apr 2025 17:16:38 GMT  
		Size: 71.8 MB (71829722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1bcbc2a14e1ef01544d5d4cf91910c417c0d7bef518d9c742ec605a2be28129`  
		Last Modified: Wed, 23 Apr 2025 17:16:37 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228c562f4bb62ea41e435246b6d8870abf8be97d5961a4827410fe2aa752d626`  
		Last Modified: Wed, 23 Apr 2025 17:16:37 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:07c9b2bc8e2614886196435517f8ddbd213cdbbda78f168a74be1b9f6a3ae4a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4880483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf62186da61c69c874ae7b27453a7b9845ca888dc2655cdb2fc826cb9373bcc0`

```dockerfile
```

-	Layers:
	-	`sha256:f5c57671d5588c42f2771e646ff7a62bf62ab90a28d4cb92a3789cb687b5f603`  
		Last Modified: Wed, 23 Apr 2025 17:16:37 GMT  
		Size: 4.9 MB (4864611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95bbdbb1fe0046be3dd208c80d11d62ab07cff6deab5a683ce6e20bf2972c7ab`  
		Last Modified: Wed, 23 Apr 2025 17:16:37 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bookworm-slim` - linux; arm64 variant v8

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

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

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
