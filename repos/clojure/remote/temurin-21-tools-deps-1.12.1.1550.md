## `clojure:temurin-21-tools-deps-1.12.1.1550`

```console
$ docker pull clojure@sha256:809a6f7f0295906fcb677ffa088b5c998e86b7e6eb4beb4805ee8c4ba1ab7b40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.1.1550` - linux; amd64

```console
$ docker pull clojure@sha256:80702d6e583a099dcc959f86727d822dac047089671f4bc05ceea18cacb60b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287117239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c29e11773b1003dfd5faa554c02b0ff3265f25960ffcdbdc38ee741942bdde`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fd67c21761eeea853e1325ede134b64185cdbe41edb316870299d3e74bf663`  
		Last Modified: Mon, 09 Jun 2025 18:58:37 GMT  
		Size: 157.6 MB (157634498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90928782de3d967ea76c5946dbcd5c6afd9ce59c4b8709da7262d43be6930f2f`  
		Last Modified: Mon, 09 Jun 2025 17:18:59 GMT  
		Size: 81.0 MB (80993456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfe49168964215b4c6a2ecd7e1b50fcfc6e4d0cd5086e74bc9e56bc8b214c73`  
		Last Modified: Mon, 09 Jun 2025 17:18:49 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebc6276d584c41fed9045d119379cb5e712e64085664199e74aaf6d8343c18b`  
		Last Modified: Mon, 09 Jun 2025 17:18:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550` - unknown; unknown

```console
$ docker pull clojure@sha256:e67c4d11b70067fb55d57ea76378ab80da8c13947ba7a39a3fa1c2fd64e08056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7389835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9887becbffa37436c6a0f78d657ce969eb5853740c95ca89b66ca780cfd4ff54`

```dockerfile
```

-	Layers:
	-	`sha256:c837fbfa79ba0762500012f4741f1c2f2471bbf077ebe7bcf69bb3337fd7d5ea`  
		Last Modified: Mon, 09 Jun 2025 18:38:59 GMT  
		Size: 7.4 MB (7372014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f35e1bac0054971d7fdb8f983a8b0ec737a15de3d6b7405a80ae3d32a0f9d29b`  
		Last Modified: Mon, 09 Jun 2025 18:39:00 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.1.1550` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9f2841492bc2a78d4f1fd18e2ad8c6488ba7e6c5bffa35b8864e72e8c44f4a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285105433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d2be68f20f2b8921d12753de69cb433a6302f362e359e5bf5c7b2a4bdda543`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437f8f7a50b2952398084c7b3ca28b3cfe6e72e05419b0e1b568927135d80a2d`  
		Last Modified: Tue, 03 Jun 2025 13:43:18 GMT  
		Size: 155.9 MB (155928814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc56d3d10045d4b80aad14367c0bba9da6bf23ec008de1ea2f71d8cadfa23577`  
		Last Modified: Mon, 09 Jun 2025 17:52:08 GMT  
		Size: 80.8 MB (80848398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12cfdd202cbef614fa13b0585d78f42db8d32b3ae4fdf52ea5a585824b625c0`  
		Last Modified: Mon, 09 Jun 2025 17:51:59 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c29a9e81dad7c0101024863e951557744f7b0f3d09e644f565f8e25ac38ff23`  
		Last Modified: Mon, 09 Jun 2025 17:51:58 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550` - unknown; unknown

```console
$ docker pull clojure@sha256:de60972c32bb46258cde5cb3534298b63305c07a88ff85ddad51cfbd77086bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b6efd9c5e1b47e2e06ec0271008f815cf77a1059fa9944e3adf54edca57e1d`

```dockerfile
```

-	Layers:
	-	`sha256:d9e87165dcc4b7d405aef5b84301cfb8693b72826628b80f172e08495fab287f`  
		Last Modified: Mon, 09 Jun 2025 18:39:07 GMT  
		Size: 7.4 MB (7377849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5e33394a2a781bbe7eef1dd6533a04127b19c9134929ea1bbfc8d8dacbe46b4`  
		Last Modified: Mon, 09 Jun 2025 18:39:08 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.1.1550` - linux; ppc64le

```console
$ docker pull clojure@sha256:32088479daa841a6aee0cf70b1022f58c5534a7a09da5c0e6a4248b05f45b961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.0 MB (296950988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124b545b706585f813a1544ba7e98ee0562b68b12aaec31c4b463fa593a041a5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Tue, 03 Jun 2025 13:33:40 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860dcfb7182a5dc32b212ca727ac1ab0a7e7f5698fd7540ceb4c7f84c97337da`  
		Last Modified: Mon, 09 Jun 2025 03:22:39 GMT  
		Size: 157.8 MB (157804869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343ae8cef8e12d2af44b1b62d7c140751e2f60942b96e3914ceac3c1a2c41ef1`  
		Last Modified: Mon, 09 Jun 2025 18:11:19 GMT  
		Size: 86.8 MB (86813457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a74502f76ea04e67e70441fe5b18368f3ae5944b7e85a00746928398a3e8aa`  
		Last Modified: Mon, 09 Jun 2025 18:11:10 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0089c96883885602ebb29facce2302fcbba625b3f6c84a4ae82a3d2d26b86286`  
		Last Modified: Mon, 09 Jun 2025 18:11:10 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550` - unknown; unknown

```console
$ docker pull clojure@sha256:82d6a542af54c7e17f4ee4a8a9398e87e4f146b04f292f43628f5da12ea072e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30614ee91cd78aaa5845cf934a422cb5914c62fc07eb168cb0d0bda99675658f`

```dockerfile
```

-	Layers:
	-	`sha256:03b192c1179a03a0629fb9f22e3402312bc100ca57c96f51d122cbc689877415`  
		Last Modified: Mon, 09 Jun 2025 21:37:25 GMT  
		Size: 7.4 MB (7377254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee9650792ef0aad6cbcd80d2aec295733b37bf88ed11cf82fbbb645923abbddb`  
		Last Modified: Mon, 09 Jun 2025 21:37:26 GMT  
		Size: 17.9 KB (17905 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.1.1550` - linux; s390x

```console
$ docker pull clojure@sha256:f586ad30fb8c4ee6488b1ba684062862a6c63e8ec0e55369cc81b30a022eb006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.9 MB (273858560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97063150547c67af2279964dd38ccd8ed0fdeb44bb77ee4b129d23a9ce03f34d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Tue, 03 Jun 2025 13:33:39 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0351b5becfe334f70decb5f4368fae95fc08263ea48dd42b0157f6c4565135db`  
		Last Modified: Wed, 04 Jun 2025 11:31:46 GMT  
		Size: 146.9 MB (146911002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fbc78b5923aed89eae10ac6469c5ad781d4e204dcd2dcc3ad2f6c4fc8bd411`  
		Last Modified: Mon, 09 Jun 2025 18:52:13 GMT  
		Size: 79.8 MB (79802673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03a9c9c950b0edba3ba1a734847d937aa75ca7d995c96d2cceed9a831158af9`  
		Last Modified: Mon, 09 Jun 2025 18:52:06 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163a4b74e2fd9e5c9611e43ffb3cede07ac4a24189871aad63f7058bc5c510a6`  
		Last Modified: Mon, 09 Jun 2025 18:52:08 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550` - unknown; unknown

```console
$ docker pull clojure@sha256:89a2773b727783f6814d44c5344d6261a86250122279426118f3e3ee4d929424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7381154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb6cc1174c6a79c21277deed23ae2cadd63eeace0784e61ef0dfb90d86e94409`

```dockerfile
```

-	Layers:
	-	`sha256:20c547e7a77c151a4223e76d23713436cd3a36b8396c7faaeca3e55347798ed7`  
		Last Modified: Mon, 09 Jun 2025 21:37:32 GMT  
		Size: 7.4 MB (7363333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:182d73f23b74937a9c24dacbc50483100055a8fcc4f4fae06d440ecbb1c7d5b6`  
		Last Modified: Mon, 09 Jun 2025 21:37:32 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json
