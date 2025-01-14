## `clojure:tools-deps-1.12.0.1495-bullseye-slim`

```console
$ docker pull clojure@sha256:75b7a991b39b1205dab9f92694c911a5bdecb0255fea4857440becea0151bf57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.0.1495-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:427bcb6826ee0194ae878f3bf05577f555ce7b78c3275a5d12e24e657cc69255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246603453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2e4c68807e55d4272f3e35f78086eeea0e88390178619afb266aec3eb16d90`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
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
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba59a1c7668dce28d1c28730c1dd7443b8851e3a7a8ebe55eeaa88f85957bb60`  
		Last Modified: Tue, 14 Jan 2025 02:44:50 GMT  
		Size: 157.6 MB (157568721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:576877e3014abd29fd58756036d04ceca54070f83921a94b10198d6bed817b4c`  
		Last Modified: Tue, 14 Jan 2025 02:44:48 GMT  
		Size: 58.8 MB (58781026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0254f25c380b2c95dfc0457b4b6767e2e41569a4c287ca7ecc5737385d47355c`  
		Last Modified: Tue, 14 Jan 2025 02:44:48 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d373cd8299194d66d429115b2afcb8d4ccedc165c130d6bf372fd6ee330dbf13`  
		Last Modified: Tue, 14 Jan 2025 02:44:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1495-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f56d9582e52ad00fde04146264a645e6e2fccf48485b8c6d0a1a0519d53514d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3051ea551d6b5faffdc1850ca3715c9f6cba5ffe861daa22091c5601ebcc577`

```dockerfile
```

-	Layers:
	-	`sha256:3d906c6acbef50f1f5c6218fe3771df62cd2e5b149c5d6b115a63d6d36cf2818`  
		Last Modified: Tue, 14 Jan 2025 02:44:48 GMT  
		Size: 5.1 MB (5120867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:517415be3eea0a09f436993984bec28b72ccb3629870dd1ecfb3a035ca1b1bf4`  
		Last Modified: Tue, 14 Jan 2025 02:44:48 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.0.1495-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:103d0daebb625b4a7bc0bd6df14b799bcd97ae4db6c784a94b812944adacc6c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243444177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3931701b93f7f50ce41603ccabbbffb77da6617ffd077a547456c9d48f553010`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416a3a2fd8cd9807260966b02586a95c093ce6d1bd3085e2276d72f97ddf05cb`  
		Last Modified: Wed, 25 Dec 2024 07:33:18 GMT  
		Size: 155.8 MB (155793154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507e7d736a8a13a2d9a49ebebffd14c83ee9ef03b8bd7b7dec5827ce4c6da41f`  
		Last Modified: Tue, 07 Jan 2025 03:33:49 GMT  
		Size: 58.9 MB (58905129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b6260e195928fc38cdb9e75b89fda2baf3771903469963fb93fbcab0fdccd7`  
		Last Modified: Tue, 07 Jan 2025 03:33:47 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd47f052b304cccc68cde06c9f6ec1bf0a0c55ad0c6b7f5be1cdd524dd213fa`  
		Last Modified: Tue, 07 Jan 2025 03:33:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1495-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:edb4e9e380039043b74148a92094147ab76965cb4a31fd43c3fcd9e6cf41c56c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5143340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa3aec82c02313e939825639e5031860e3b219051872014358321d4576aef98`

```dockerfile
```

-	Layers:
	-	`sha256:8cabcd7de38d8ad996b04162ee46a9d3d1843760eccc9e06642a65e0787fef1b`  
		Last Modified: Tue, 07 Jan 2025 03:33:48 GMT  
		Size: 5.1 MB (5126623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4651d1fbb5490cda49ecf8bc0ed060acc4077296bbf89fbda1069ff96e9c4ef3`  
		Last Modified: Tue, 07 Jan 2025 03:33:47 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
