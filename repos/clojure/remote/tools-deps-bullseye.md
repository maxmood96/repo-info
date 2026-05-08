## `clojure:tools-deps-bullseye`

```console
$ docker pull clojure@sha256:136f5dc25a39edcbfd450ebc7ed40ae77538d61a2d8028fa54bf26c188e36714
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:a2cae2747822a5cedf814db39afe744d3df6be41747b99a04bd3d4f31aa3b987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.9 MB (215936494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e60b6800d0b94e46cdb3a37ebf32f55abb98b0b6cfb69b47e876a4c9a23609`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Thu, 30 Apr 2026 23:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:53:36 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 30 Apr 2026 23:53:36 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:53:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 30 Apr 2026 23:53:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 30 Apr 2026 23:53:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:53:50 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:53:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ac264864efc6e224f48927519c232d58db17298271d49eec8ab97f78c33057`  
		Last Modified: Thu, 30 Apr 2026 23:54:11 GMT  
		Size: 92.6 MB (92574623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9004b6562d57ee3494af308fb13557ff1f9cb74cd5fbada438a61c6c5357aa73`  
		Last Modified: Thu, 30 Apr 2026 23:54:11 GMT  
		Size: 69.6 MB (69597679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b651216a89212837ca7a2cd184c62c9b55221ecc7b6eb7f8129185ed76328ae9`  
		Last Modified: Thu, 30 Apr 2026 23:54:07 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13090d588a1ef0e543eb60543f2c23dd9608b6176019d5287b12258572178c5e`  
		Last Modified: Thu, 30 Apr 2026 23:54:07 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:db5382d165d5181ddc641aaeb1779a95c9a226f777ac30ced950af34c8056700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7392797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7bf3b4110fef5c1a24ef957dc9456b870b656d0989c0e72752b7530908f295`

```dockerfile
```

-	Layers:
	-	`sha256:bbf00ae76121e6f15a0a4f4cf8331d6b40308ee389d3b0763d5571eef381753b`  
		Last Modified: Thu, 30 Apr 2026 23:54:07 GMT  
		Size: 7.4 MB (7376350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3376c67b4b950ed16db01d6ad0d7de8b862ca1007c086e5c192332632e910b08`  
		Last Modified: Thu, 30 Apr 2026 23:54:07 GMT  
		Size: 16.4 KB (16447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c6e967fecc52877b38f03dea72fca4f2f9a138a06b24860af04b24eb37a3a6ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.5 MB (213534815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70750c5529a79450b4487b9b0ab302835fe11c411087386d79ee361c8d6d037`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:27:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:27:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:27:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:27:40 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:27:40 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:27:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:27:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:27:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:27:54 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:27:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5344866c8ac687a28040c00d8bd15d6f6eb85e6470fbf5064a9c0f10e49391bb`  
		Last Modified: Fri, 08 May 2026 00:28:15 GMT  
		Size: 91.5 MB (91542292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081bd10db25731ef1df7ac017c96abf26f3af8067175f335074c4815d985b153`  
		Last Modified: Fri, 08 May 2026 00:28:15 GMT  
		Size: 69.7 MB (69738477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73f6bfdb23ee1d9f987144a173c268e085a052dbfbb315f4fe9d510e0775718`  
		Last Modified: Fri, 08 May 2026 00:28:12 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8f9035b9b17ee934ae7716989e58d4f6749111b2014806d7f9d4c1c8a2427a`  
		Last Modified: Fri, 08 May 2026 00:28:12 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c8f0423329b82c8dcba0dd782a717789cfec63e3797256b0e5d97af344a51991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7398213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071f23410dce57bdef6bf996fb631ce9a52aa4fea0f176fb1159be5f47825319`

```dockerfile
```

-	Layers:
	-	`sha256:516a6877d7e855a505f6e0272b5ac27c76fcc21137ccfedd2e419a5c8f3e6013`  
		Last Modified: Fri, 08 May 2026 00:28:13 GMT  
		Size: 7.4 MB (7381470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7128f643edbca1a06be66f9a87a136c522e9872d62cbbb7c889a9efa6e43c122`  
		Last Modified: Fri, 08 May 2026 00:28:13 GMT  
		Size: 16.7 KB (16743 bytes)  
		MIME: application/vnd.in-toto+json
