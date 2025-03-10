## `clojure:temurin-23-tools-deps-1.12.0.1530-bookworm-slim`

```console
$ docker pull clojure@sha256:4728d82ebd04c0214fbeeadd084542ab804649815505763c9a36f16ba505e92b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1530-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5f231be50764280969944727c2056118943b56e66514cbee3b25ac0405b19758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263063999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:044666ad3b126f9faaa4cf3e9fccdc2e19082fabb31989bfa6856a0462b581a4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069596e310dfe895da22fe6575b69b2ccfd2b388d3ae220fd6fd90de51854dec`  
		Last Modified: Mon, 10 Mar 2025 17:40:23 GMT  
		Size: 165.3 MB (165316201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85d0ecd8b2ac212c1c3e0d65e5752cfb99a77d2f3cc59545928bfd011e3f64e`  
		Last Modified: Mon, 10 Mar 2025 17:40:21 GMT  
		Size: 69.5 MB (69527455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e6d2f242046fa1ed63dbd24ea80654f6b1654f3883cc38b53d1404cf8824f4`  
		Last Modified: Mon, 10 Mar 2025 17:40:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c1839af282a0c7d0ddb1763ef53e09b25b8fd46eb8c8c8b15601494c4a5b77`  
		Last Modified: Mon, 10 Mar 2025 17:40:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0656cc9d9041f15bc92f2d5652ac1b1106529b5a40a849c13da0b6c8298bac09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4933468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852dfb38e9cc026bb49488048a03ecbea24209c47d6284af057ca8fc89077873`

```dockerfile
```

-	Layers:
	-	`sha256:9d6ee02bd1872e487f125957891b1bbde4328f4243922782fcf0f4277bb24967`  
		Last Modified: Mon, 10 Mar 2025 17:40:19 GMT  
		Size: 4.9 MB (4917590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f231aec426cd57a83fe0262de4a55dc4b0b0dd1367208d2cc4e0a3a19c1eb247`  
		Last Modified: Mon, 10 Mar 2025 17:40:19 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-1.12.0.1530-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:39584511918dede1898b70004afae51f012ce1482051ba879f1850a92ab92aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.8 MB (260769377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c153932c6ac85fdc348ae6057a0ca78f9ac0dc36be18d91a51d32b0e80e19414`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c63e38e64abbce83edb1dd8652ca693685d46761d360ce2d37e4cff9f97c9f9`  
		Last Modified: Mon, 10 Mar 2025 18:00:03 GMT  
		Size: 163.3 MB (163341423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2a12fe3bb63bbc0a6a77086609ff0deaa59e634044e10c98723ef1608c6477`  
		Last Modified: Mon, 10 Mar 2025 18:00:01 GMT  
		Size: 69.4 MB (69378482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545ef110421f3e14630cea093b4d43a2d0c8f27be13c15b606ded436dfe7777c`  
		Last Modified: Mon, 10 Mar 2025 17:59:58 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c9c5623fbfd52a814eb7dbff36ac17eee574335e4b5385c1ba5d447b8f1c07`  
		Last Modified: Mon, 10 Mar 2025 18:00:00 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0e1885313e98e9ddc07ca42dc72b4cfbba67084f87581fab98ac6fe95f7fd02d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4938725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5abd1a6bc7a30d6e84557a44ffea728f186dbd79b68432d5c1325d519ddf3aec`

```dockerfile
```

-	Layers:
	-	`sha256:cf64761852a503040d5e0faed5365a4678c113f3a2d7830406e2405351bc5b1f`  
		Last Modified: Mon, 10 Mar 2025 17:59:58 GMT  
		Size: 4.9 MB (4922730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55dd0be9b374cd674403750bd62634a4ca35d654ae103629039d60895b1d47eb`  
		Last Modified: Mon, 10 Mar 2025 17:59:57 GMT  
		Size: 16.0 KB (15995 bytes)  
		MIME: application/vnd.in-toto+json
