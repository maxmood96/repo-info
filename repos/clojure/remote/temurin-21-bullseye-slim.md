## `clojure:temurin-21-bullseye-slim`

```console
$ docker pull clojure@sha256:ebeda4d50415463fc558fa721f84acdd67fd42d4c19e88c081ea6bdb82439165
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:de1e127dd6e0ea00ca691d5ce334d4d604fbecb319bc1470596ea7ce2e87a87a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.6 MB (248580607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b92cd841ce25c236cb56611e2431c173a04dd1af62904ae6931e24777457e17`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8e7422bde1ed2c9dc2ff21b284f30d4d19480f2e0099eb53c93bd9355b3590`  
		Last Modified: Tue, 13 Aug 2024 01:11:35 GMT  
		Size: 158.6 MB (158579301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5f9bd85721a71ea257e229d246bc72c683ceaaa1592ea5b0f28af47af832c5`  
		Last Modified: Tue, 13 Aug 2024 01:11:33 GMT  
		Size: 58.6 MB (58571981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02184d236573c4693b35808f5cb6a56b1b2f983379085bdd783f7a04ebc2438d`  
		Last Modified: Tue, 13 Aug 2024 01:11:32 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a37573f68aa247c8701c0c9e3e39e82be5e069682e368b14b9a6a9cb159485`  
		Last Modified: Tue, 13 Aug 2024 01:11:32 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2f320e83e7673509e826cc6d49d708b93e3443891f6874450745756413cf70a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4966741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee219f6d8c4c07843a6add50ccfef1a6f47f4d8dc2ba5cb944f42f20b26a3da`

```dockerfile
```

-	Layers:
	-	`sha256:c4cd617c5e58fd5d90b6c1f987f1317c54d9c7a78fe452e4053e06f3673c1dbf`  
		Last Modified: Tue, 13 Aug 2024 01:11:32 GMT  
		Size: 5.0 MB (4950532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3f02cb94e83d4d7babd6eaf94abd20e36960c5567f455e943d956b892a2b575`  
		Last Modified: Tue, 13 Aug 2024 01:11:32 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:92ae971ee3ec6cbec99ffe94fc43e6dddc7934c9c334b603b483a91984134f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.5 MB (245523066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c868bbe3cbb8e869022c36c11db58b1695252769c04ef8274ef74f0f139ca484`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jul 2024 04:18:06 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Tue, 23 Jul 2024 04:18:07 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1809c9c43cb8a5d38ddcdceca82616c1c0ce8b228c7a20f60893aa6dad9b1104`  
		Last Modified: Thu, 25 Jul 2024 21:19:59 GMT  
		Size: 156.7 MB (156746183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a832cf9849ed8c85dcb6a10e5dc981d38b2422aea1529759785c8825140fa2c`  
		Last Modified: Wed, 07 Aug 2024 20:14:29 GMT  
		Size: 58.7 MB (58699756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff616fdf0f0ffc1c747e4369fe39d0fbb92cb85ed9fd4e7078b5ec624040d495`  
		Last Modified: Wed, 07 Aug 2024 20:14:28 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4200834e29773aa76f8cc701b65963a09a6d2f9498f25d72169d521d2836687a`  
		Last Modified: Wed, 07 Aug 2024 20:14:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a0a1f1f4c59f3a2822488475a9cbfeb3b3c3976a3c42fcb22970353fc0ab7bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4973686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82cdb29a4c0154bfb1e06b66608137aad355594eb4f34483b3429aa509343f0d`

```dockerfile
```

-	Layers:
	-	`sha256:1a5734e50c564a450284db1deb019350386c0620c2bcc4f95a391c4f790430d3`  
		Last Modified: Wed, 07 Aug 2024 20:14:28 GMT  
		Size: 5.0 MB (4956912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1682ab611f991ef2d6d72e85f39ae6fe18ff9825c164be728a31fee959551054`  
		Last Modified: Wed, 07 Aug 2024 20:14:28 GMT  
		Size: 16.8 KB (16774 bytes)  
		MIME: application/vnd.in-toto+json
