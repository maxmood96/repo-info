## `clojure:tools-deps-1.11.4.1474-bullseye-slim`

```console
$ docker pull clojure@sha256:71516a2d3bf4392157f1942f1f86b0fcf2f36e0897303506c9ef160ef8505127
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.11.4.1474-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7f6f66266067e96086f3a053dabe34732abb300eff3d58e6136013c5c0ba3185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.7 MB (248710995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff7786c056d2323224919f12a4608324b416766e7fb3678df56bfad115fd3f3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
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
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29dcb078d61094cc98ff031efcf9ec666ad68d9ba6f3ed26700aef929eed23ec`  
		Last Modified: Wed, 04 Sep 2024 23:07:57 GMT  
		Size: 158.6 MB (158579224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb57597edefedf9280d211300ec959aaf6ef022091b9d282020a55c4494cd29`  
		Last Modified: Wed, 04 Sep 2024 23:07:56 GMT  
		Size: 58.7 MB (58702055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e60d9db781a32fe1a4ebab0f386d6266e922a5ee323bc925bddad639bb81311`  
		Last Modified: Wed, 04 Sep 2024 23:07:56 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecb174580a68155fdc26b194b580db496a7caeed90dcaaccb92cea1b16d4509`  
		Last Modified: Wed, 04 Sep 2024 23:07:56 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.11.4.1474-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:aef7facd2bcf326a59708746979cc60b06a5d538745f77fef80b50af154f527e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4966741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7d99752c6f239549638577b060a834058bff01d0f2b5a3bd4ffa7549d1ccc7`

```dockerfile
```

-	Layers:
	-	`sha256:2fb49a9e2b9ffb55020ac24a78fc98b15c8cedca97e548f7b57623d754a1c3f4`  
		Last Modified: Wed, 04 Sep 2024 23:07:56 GMT  
		Size: 5.0 MB (4950532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e967e81b9389658c133ab2a2f5ac0a02f943293d62c18523ba16a39e21807ee9`  
		Last Modified: Wed, 04 Sep 2024 23:07:56 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.11.4.1474-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2318980d67b017633df45abf78b85ebaf83b29ca5ed4e99f6d2132f6864a2082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.5 MB (245522993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ef562354eb9ba7512d69a39c8f84efe34db184b440a31b432613f2737ef979`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
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
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b15530537a9dd5edfec936a719ec37d545d451060f2c3d9a669c1b6403ac7d`  
		Last Modified: Sat, 17 Aug 2024 06:24:00 GMT  
		Size: 156.7 MB (156746187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affb1de15585d16d53a483cb2f877e679dc82cf5ac2e8f5a8085e07ffcfb48ac`  
		Last Modified: Sat, 17 Aug 2024 06:30:08 GMT  
		Size: 58.7 MB (58699676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560cf99de31e05c293c006c027aea990044fdeafd17480674b5ff65aca9ce120`  
		Last Modified: Sat, 17 Aug 2024 06:30:07 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139f5c105c734e327cd0fa80ca774357c1bd86663a13af81d097c3bc6587f450`  
		Last Modified: Sat, 17 Aug 2024 06:30:07 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.11.4.1474-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1acb206d7f0d06a4ec7cc079aa25596cce589c67fb4d0447181b6aaffdcbe317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4973686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7da746e23c9a4d62cb95779370f010c5f88f1f51c5e2cb37ef08df68d9fc474`

```dockerfile
```

-	Layers:
	-	`sha256:94554a1de6188f9aff9dca55a66affd3896fbdb4cd7bceffcd9baf40dfab9fc0`  
		Last Modified: Sat, 24 Aug 2024 00:08:09 GMT  
		Size: 5.0 MB (4956912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddfa9a1f24b752982144561d71d636bc88b19179d4abef2a816c39affd71b93e`  
		Last Modified: Sat, 24 Aug 2024 00:08:09 GMT  
		Size: 16.8 KB (16774 bytes)  
		MIME: application/vnd.in-toto+json
