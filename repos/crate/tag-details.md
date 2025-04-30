<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:5.10`](#crate510)
-	[`crate:5.10.5`](#crate5105)
-	[`crate:5.9`](#crate59)
-	[`crate:5.9.13`](#crate5913)
-	[`crate:latest`](#cratelatest)

## `crate:5.10`

```console
$ docker pull crate@sha256:58d66d48e2782ce0c8043ca4fa0ebbaa1c0131dc3a432fa1f2a93e1f0215e6e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.10` - linux; amd64

```console
$ docker pull crate@sha256:e65439e3e202c575884f4c339cbb99e024adbe41363e4e555381ec97ff6be4ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233714481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a81914b407121b241cab29bff673994a23acfdb75513c8e9f4f72a7fa6667c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 07 Apr 2025 13:02:24 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 07 Apr 2025 13:02:24 GMT
CMD ["/bin/bash"]
# Mon, 07 Apr 2025 13:02:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 07 Apr 2025 13:02:24 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.4.tar.gz.asc crate-5.10.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.4.tar.gz.asc     && tar -xf crate-5.10.4.tar.gz -C /crate --strip-components=1     && rm crate-5.10.4.tar.gz # buildkit
# Mon, 07 Apr 2025 13:02:24 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 07 Apr 2025 13:02:24 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 13:02:24 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 07 Apr 2025 13:02:24 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 07 Apr 2025 13:02:24 GMT
VOLUME [/data]
# Mon, 07 Apr 2025 13:02:24 GMT
WORKDIR /data
# Mon, 07 Apr 2025 13:02:24 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 07 Apr 2025 13:02:24 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 07 Apr 2025 13:02:24 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 07 Apr 2025 13:02:24 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-04-07T13:02:24.481728 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.4
# Mon, 07 Apr 2025 13:02:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Apr 2025 13:02:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 13:02:24 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:a3fe057ad103398a19e5279ad7d72ce89b6fe2cafdc6602093481d014edc3819`  
		Last Modified: Mon, 14 Apr 2025 21:04:12 GMT  
		Size: 66.7 MB (66703326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e0ec4e85910e88ae5693be014495ddfcfb4d475413e9445da83be4324d13ba`  
		Last Modified: Mon, 14 Apr 2025 21:08:03 GMT  
		Size: 15.4 MB (15404567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb68b039267d216928d8f470bab57d8012f1c48ed2ee62889f652d749139d498`  
		Last Modified: Mon, 14 Apr 2025 21:08:05 GMT  
		Size: 149.7 MB (149661079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206ded9a16680ed8662e12fb43d974b450e6627387db1f6f79397fc17c318fa3`  
		Last Modified: Mon, 14 Apr 2025 21:08:03 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c0876332de2d3cfda56b7110f93963d12ea24d04d604a549ba92950b2cfb00`  
		Last Modified: Mon, 14 Apr 2025 21:08:03 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1beb8adcd8fa5e9ec7a21a9d70e117d16c8246f6a5e6c9c08eed4940b53992aa`  
		Last Modified: Mon, 14 Apr 2025 21:08:04 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2088c0fa8e3ae16ed456ed52417639e717ea1becebe8eaba76d7608052ed7bf`  
		Last Modified: Mon, 14 Apr 2025 21:08:04 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d5fde7835c372320167f48ba6385f315385a37075ff26a0a97c8eb040529bc`  
		Last Modified: Mon, 14 Apr 2025 21:08:04 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:dfeefc048ba73a506973cf4fb5719a53876e859edc93515c5ddf1f4e255e6bde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5192575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdea4f9bdeb1c8bdff78ff63d659f155a2194328658838a8f8b6ad7bf9ac1eff`

```dockerfile
```

-	Layers:
	-	`sha256:3d8c87f1a34eb1ea8be9b7a03256535710392c52ef7bc5f908eb6cd53dd96ae3`  
		Last Modified: Mon, 14 Apr 2025 21:08:03 GMT  
		Size: 5.2 MB (5169375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:089b961f9192e09d23d7373bd2ceb12c727e948ba90ef7882d8d2d9dcbd35474`  
		Last Modified: Mon, 14 Apr 2025 21:08:03 GMT  
		Size: 23.2 KB (23200 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.10` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:3097bcc5574fdc845ab8c22af2279cabadaa76ae55a2d43603f77687fa098975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232993387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ea2e63d0e02be53561ded6f060ebf3936e0c7cb78b4cbfd1d7b95c43411eb5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 07 Apr 2025 13:02:24 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 07 Apr 2025 13:02:24 GMT
CMD ["/bin/bash"]
# Mon, 07 Apr 2025 13:02:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 07 Apr 2025 13:02:24 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.4.tar.gz.asc crate-5.10.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.4.tar.gz.asc     && tar -xf crate-5.10.4.tar.gz -C /crate --strip-components=1     && rm crate-5.10.4.tar.gz # buildkit
# Mon, 07 Apr 2025 13:02:24 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 07 Apr 2025 13:02:24 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 13:02:24 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 07 Apr 2025 13:02:24 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 07 Apr 2025 13:02:24 GMT
VOLUME [/data]
# Mon, 07 Apr 2025 13:02:24 GMT
WORKDIR /data
# Mon, 07 Apr 2025 13:02:24 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 07 Apr 2025 13:02:24 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 07 Apr 2025 13:02:24 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 07 Apr 2025 13:02:24 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-04-07T13:02:24.481728 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.4
# Mon, 07 Apr 2025 13:02:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Apr 2025 13:02:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 13:02:24 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:443342f58da70c4d8462137201b4af95fe44752374fc07fa7f48092fcf802c88`  
		Last Modified: Mon, 14 Apr 2025 21:03:41 GMT  
		Size: 65.2 MB (65245289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174a192bbbdb738a0ab32cb314abdd2dc66239fe7bb1be4022e0a269ef6131f2`  
		Last Modified: Mon, 14 Apr 2025 21:08:02 GMT  
		Size: 15.5 MB (15465210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc7d1decbd1df988122ca4c85068fd891fb73bea4909c571600cd357a2a667e`  
		Last Modified: Mon, 14 Apr 2025 21:08:07 GMT  
		Size: 150.3 MB (150337372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce7acc7e87cb19c1d3ceaf625fc1c6b777ce40f2714bf69362a183c3313dca0`  
		Last Modified: Mon, 14 Apr 2025 21:08:02 GMT  
		Size: 1.9 MB (1943638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dbe8d0c630dfb805c9811c857a338a93de5de42f5962fe80ea12325dd45258a`  
		Last Modified: Mon, 14 Apr 2025 21:08:02 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff573f00ba40b5fc1eb24052e0c0e257dc62bb57a3724cfdf07fc1ae5c210db`  
		Last Modified: Mon, 14 Apr 2025 21:08:03 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138f2b97cc07c8af616136e8d1e8d58366ac43d8078ded85b63623bd4fc1f976`  
		Last Modified: Mon, 14 Apr 2025 21:08:03 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ec8cb1b52f832401db024039718321c05e1cbb7802aa8db65660548682f119`  
		Last Modified: Mon, 14 Apr 2025 21:08:03 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.10` - unknown; unknown

```console
$ docker pull crate@sha256:c81866383522b7781484f6c60fc38a84a5332e7bff9160d51d3a9c55b753ab4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7870e0a06cbea8842ff48b582ecf29a75b41c14847bbae355621317f47ff6cdb`

```dockerfile
```

-	Layers:
	-	`sha256:ae5aa980d963eec3d20ba72a556265686279d59c634c3324c25ca370ff967e8a`  
		Last Modified: Mon, 14 Apr 2025 21:08:02 GMT  
		Size: 5.2 MB (5166683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:655b6fac11315b4ced84bb93d68c4964da086d4c04aab5a6fc1a5be4e52f82c5`  
		Last Modified: Mon, 14 Apr 2025 21:08:01 GMT  
		Size: 23.3 KB (23338 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.10.5`

**does not exist** (yet?)

## `crate:5.9`

```console
$ docker pull crate@sha256:ffedbc7974cda08786c0c947ea192abe597a1ba15538d9bb4edbbf494cc847f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9` - linux; amd64

```console
$ docker pull crate@sha256:f537194f75e09dbadb3f50f8cf3b34b55cf715af664a7bcf1afafc12adf36c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233063168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62c2f8d2990e1a7e79992d2fadda933f90c212b968dd92cf8fa6c8a9745d03eb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 07 Apr 2025 11:11:57 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["/bin/bash"]
# Mon, 07 Apr 2025 11:11:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.13.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.13.tar.gz.asc crate-5.9.13.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.13.tar.gz.asc     && tar -xf crate-5.9.13.tar.gz -C /crate --strip-components=1     && rm crate-5.9.13.tar.gz # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 11:11:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 07 Apr 2025 11:11:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
VOLUME [/data]
# Mon, 07 Apr 2025 11:11:57 GMT
WORKDIR /data
# Mon, 07 Apr 2025 11:11:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-04-07T11:11:57.278779 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.13
# Mon, 07 Apr 2025 11:11:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:a3fe057ad103398a19e5279ad7d72ce89b6fe2cafdc6602093481d014edc3819`  
		Last Modified: Mon, 14 Apr 2025 21:04:12 GMT  
		Size: 66.7 MB (66703326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcec82adec80585ecd662ca78a0a2f00f1915f54a14c46e5fffbae3da506f64a`  
		Last Modified: Mon, 14 Apr 2025 21:08:12 GMT  
		Size: 15.4 MB (15404609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3397a7a4a1589583fca2b027400b84db10a3df5d76a6761164d5fdc8915d8636`  
		Last Modified: Mon, 14 Apr 2025 21:08:14 GMT  
		Size: 149.0 MB (149009725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16ff60c8defcb75fcd4b47eda730704b25042bf0bacdd26db044716c5f44967`  
		Last Modified: Mon, 14 Apr 2025 21:08:11 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e702fe00bb48c1f7ff88c7d399496d68fd6246a4b4c0630e662082520ef858d`  
		Last Modified: Mon, 14 Apr 2025 21:08:11 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9feb77d490a22bdd1bff757b7c07083b03249581bcb3de663375ef4a1d681fcc`  
		Last Modified: Mon, 14 Apr 2025 21:08:12 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3591542bf015fde66b8971c54f001a925cac5bb54356d0c6ccd3c525ac1f5796`  
		Last Modified: Mon, 14 Apr 2025 21:08:12 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ba8241687644aaee953c448171863ea247ab515a040b7dd1ffbc9d18f13f49`  
		Last Modified: Mon, 14 Apr 2025 21:08:13 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:fc0119993a2e866843babd9ff37f9006ee11e5684564d4a1ba48f2c2deba6101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8f9fcd3f5b0c955a620d476cac862dd9c5cd156f826e96268265d0d6c95da40`

```dockerfile
```

-	Layers:
	-	`sha256:37ac76c12023fccc6ff552b2d6b0fd0c5a8b7aad3a757b5a784f5a4bb1d89fe5`  
		Last Modified: Mon, 14 Apr 2025 21:08:11 GMT  
		Size: 5.2 MB (5167203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:332cc5481986c82035b0ef8fe8c21a9d63453825901ef3a7e3da29051e4480ca`  
		Last Modified: Mon, 14 Apr 2025 21:08:11 GMT  
		Size: 22.9 KB (22903 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:929a78a846c2a43d7b2f11e10210e165f71521c46ad85dfd9dea7a975dc861f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232364545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d635f02244bb4a41091db9633e88c9c89553ffc1e9f0d1c40d718c31b6effa5a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 07 Apr 2025 11:11:57 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["/bin/bash"]
# Mon, 07 Apr 2025 11:11:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.13.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.13.tar.gz.asc crate-5.9.13.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.13.tar.gz.asc     && tar -xf crate-5.9.13.tar.gz -C /crate --strip-components=1     && rm crate-5.9.13.tar.gz # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 11:11:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 07 Apr 2025 11:11:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
VOLUME [/data]
# Mon, 07 Apr 2025 11:11:57 GMT
WORKDIR /data
# Mon, 07 Apr 2025 11:11:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-04-07T11:11:57.278779 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.13
# Mon, 07 Apr 2025 11:11:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:443342f58da70c4d8462137201b4af95fe44752374fc07fa7f48092fcf802c88`  
		Last Modified: Mon, 14 Apr 2025 21:03:41 GMT  
		Size: 65.2 MB (65245289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174a192bbbdb738a0ab32cb314abdd2dc66239fe7bb1be4022e0a269ef6131f2`  
		Last Modified: Mon, 14 Apr 2025 21:08:02 GMT  
		Size: 15.5 MB (15465210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae080b7caf812fac4b8cf6a830e6c1b4c939f9879b6d496e0d9a78165f45be0`  
		Last Modified: Mon, 14 Apr 2025 21:08:55 GMT  
		Size: 149.7 MB (149708529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3779bc1d20dede154153f3cf11400f897cbc19e8d7f6622f42097f8cb98fe512`  
		Last Modified: Mon, 14 Apr 2025 21:08:52 GMT  
		Size: 1.9 MB (1943638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8250ea430f0db690142025bae4c5dd61e8a3658989ae0eb05ae1ee80ab39439`  
		Last Modified: Mon, 14 Apr 2025 21:08:51 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098c385c76e26e9dbd06bd1f4ce38329edcb5cd18faa6f7b47db4b4ae6ebe1a0`  
		Last Modified: Mon, 14 Apr 2025 21:08:52 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d28a23eb4d9b10fa7853258821d225981be6d2b2e20af490ed810560fe5ac1`  
		Last Modified: Mon, 14 Apr 2025 21:08:53 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e5d4d122eca3f0aed1105a90b6224bfb70eea0dae82188c88df6a6339cbd54`  
		Last Modified: Mon, 14 Apr 2025 21:08:53 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9` - unknown; unknown

```console
$ docker pull crate@sha256:07b89b44a31707eaca712262b2c15cf0a8382dfcd3b4ff74fb96df1d1caa5142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5187527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d22bc368c009dad32270ad43fca210c463741de4ad59c05767fde888bddd240`

```dockerfile
```

-	Layers:
	-	`sha256:5a271bf75c301f8293930fe7bc18dbe4c73ce087714d1ce864a16963a3d8f89f`  
		Last Modified: Mon, 14 Apr 2025 21:08:52 GMT  
		Size: 5.2 MB (5164499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b73b00e3c1dafdaf2e2dc0ce1df8b8ea7e116b330a2259e638a398c8b3e45c3c`  
		Last Modified: Mon, 14 Apr 2025 21:08:51 GMT  
		Size: 23.0 KB (23028 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:5.9.13`

```console
$ docker pull crate@sha256:ffedbc7974cda08786c0c947ea192abe597a1ba15538d9bb4edbbf494cc847f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:5.9.13` - linux; amd64

```console
$ docker pull crate@sha256:f537194f75e09dbadb3f50f8cf3b34b55cf715af664a7bcf1afafc12adf36c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233063168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62c2f8d2990e1a7e79992d2fadda933f90c212b968dd92cf8fa6c8a9745d03eb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 07 Apr 2025 11:11:57 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["/bin/bash"]
# Mon, 07 Apr 2025 11:11:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.13.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.13.tar.gz.asc crate-5.9.13.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.13.tar.gz.asc     && tar -xf crate-5.9.13.tar.gz -C /crate --strip-components=1     && rm crate-5.9.13.tar.gz # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 11:11:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 07 Apr 2025 11:11:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
VOLUME [/data]
# Mon, 07 Apr 2025 11:11:57 GMT
WORKDIR /data
# Mon, 07 Apr 2025 11:11:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-04-07T11:11:57.278779 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.13
# Mon, 07 Apr 2025 11:11:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:a3fe057ad103398a19e5279ad7d72ce89b6fe2cafdc6602093481d014edc3819`  
		Last Modified: Mon, 14 Apr 2025 21:04:12 GMT  
		Size: 66.7 MB (66703326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcec82adec80585ecd662ca78a0a2f00f1915f54a14c46e5fffbae3da506f64a`  
		Last Modified: Mon, 14 Apr 2025 21:08:12 GMT  
		Size: 15.4 MB (15404609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3397a7a4a1589583fca2b027400b84db10a3df5d76a6761164d5fdc8915d8636`  
		Last Modified: Mon, 14 Apr 2025 21:08:14 GMT  
		Size: 149.0 MB (149009725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16ff60c8defcb75fcd4b47eda730704b25042bf0bacdd26db044716c5f44967`  
		Last Modified: Mon, 14 Apr 2025 21:08:11 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e702fe00bb48c1f7ff88c7d399496d68fd6246a4b4c0630e662082520ef858d`  
		Last Modified: Mon, 14 Apr 2025 21:08:11 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9feb77d490a22bdd1bff757b7c07083b03249581bcb3de663375ef4a1d681fcc`  
		Last Modified: Mon, 14 Apr 2025 21:08:12 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3591542bf015fde66b8971c54f001a925cac5bb54356d0c6ccd3c525ac1f5796`  
		Last Modified: Mon, 14 Apr 2025 21:08:12 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ba8241687644aaee953c448171863ea247ab515a040b7dd1ffbc9d18f13f49`  
		Last Modified: Mon, 14 Apr 2025 21:08:13 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.13` - unknown; unknown

```console
$ docker pull crate@sha256:fc0119993a2e866843babd9ff37f9006ee11e5684564d4a1ba48f2c2deba6101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8f9fcd3f5b0c955a620d476cac862dd9c5cd156f826e96268265d0d6c95da40`

```dockerfile
```

-	Layers:
	-	`sha256:37ac76c12023fccc6ff552b2d6b0fd0c5a8b7aad3a757b5a784f5a4bb1d89fe5`  
		Last Modified: Mon, 14 Apr 2025 21:08:11 GMT  
		Size: 5.2 MB (5167203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:332cc5481986c82035b0ef8fe8c21a9d63453825901ef3a7e3da29051e4480ca`  
		Last Modified: Mon, 14 Apr 2025 21:08:11 GMT  
		Size: 22.9 KB (22903 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:5.9.13` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:929a78a846c2a43d7b2f11e10210e165f71521c46ad85dfd9dea7a975dc861f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232364545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d635f02244bb4a41091db9633e88c9c89553ffc1e9f0d1c40d718c31b6effa5a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 07 Apr 2025 11:11:57 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["/bin/bash"]
# Mon, 07 Apr 2025 11:11:57 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.9.13.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.9.13.tar.gz.asc crate-5.9.13.tar.gz     && rm -rf "$GNUPGHOME" crate-5.9.13.tar.gz.asc     && tar -xf crate-5.9.13.tar.gz -C /crate --strip-components=1     && rm crate-5.9.13.tar.gz # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 11:11:57 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 07 Apr 2025 11:11:57 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
VOLUME [/data]
# Mon, 07 Apr 2025 11:11:57 GMT
WORKDIR /data
# Mon, 07 Apr 2025 11:11:57 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-04-07T11:11:57.278779 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.9.13
# Mon, 07 Apr 2025 11:11:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Apr 2025 11:11:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 11:11:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:443342f58da70c4d8462137201b4af95fe44752374fc07fa7f48092fcf802c88`  
		Last Modified: Mon, 14 Apr 2025 21:03:41 GMT  
		Size: 65.2 MB (65245289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174a192bbbdb738a0ab32cb314abdd2dc66239fe7bb1be4022e0a269ef6131f2`  
		Last Modified: Mon, 14 Apr 2025 21:08:02 GMT  
		Size: 15.5 MB (15465210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae080b7caf812fac4b8cf6a830e6c1b4c939f9879b6d496e0d9a78165f45be0`  
		Last Modified: Mon, 14 Apr 2025 21:08:55 GMT  
		Size: 149.7 MB (149708529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3779bc1d20dede154153f3cf11400f897cbc19e8d7f6622f42097f8cb98fe512`  
		Last Modified: Mon, 14 Apr 2025 21:08:52 GMT  
		Size: 1.9 MB (1943638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8250ea430f0db690142025bae4c5dd61e8a3658989ae0eb05ae1ee80ab39439`  
		Last Modified: Mon, 14 Apr 2025 21:08:51 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098c385c76e26e9dbd06bd1f4ce38329edcb5cd18faa6f7b47db4b4ae6ebe1a0`  
		Last Modified: Mon, 14 Apr 2025 21:08:52 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d28a23eb4d9b10fa7853258821d225981be6d2b2e20af490ed810560fe5ac1`  
		Last Modified: Mon, 14 Apr 2025 21:08:53 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e5d4d122eca3f0aed1105a90b6224bfb70eea0dae82188c88df6a6339cbd54`  
		Last Modified: Mon, 14 Apr 2025 21:08:53 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:5.9.13` - unknown; unknown

```console
$ docker pull crate@sha256:07b89b44a31707eaca712262b2c15cf0a8382dfcd3b4ff74fb96df1d1caa5142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5187527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d22bc368c009dad32270ad43fca210c463741de4ad59c05767fde888bddd240`

```dockerfile
```

-	Layers:
	-	`sha256:5a271bf75c301f8293930fe7bc18dbe4c73ce087714d1ce864a16963a3d8f89f`  
		Last Modified: Mon, 14 Apr 2025 21:08:52 GMT  
		Size: 5.2 MB (5164499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b73b00e3c1dafdaf2e2dc0ce1df8b8ea7e116b330a2259e638a398c8b3e45c3c`  
		Last Modified: Mon, 14 Apr 2025 21:08:51 GMT  
		Size: 23.0 KB (23028 bytes)  
		MIME: application/vnd.in-toto+json

## `crate:latest`

```console
$ docker pull crate@sha256:58d66d48e2782ce0c8043ca4fa0ebbaa1c0131dc3a432fa1f2a93e1f0215e6e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:e65439e3e202c575884f4c339cbb99e024adbe41363e4e555381ec97ff6be4ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233714481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a81914b407121b241cab29bff673994a23acfdb75513c8e9f4f72a7fa6667c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 07 Apr 2025 13:02:24 GMT
ADD almalinux-10-kitten-default-amd64.tar.xz / # buildkit
# Mon, 07 Apr 2025 13:02:24 GMT
CMD ["/bin/bash"]
# Mon, 07 Apr 2025 13:02:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 07 Apr 2025 13:02:24 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.4.tar.gz.asc crate-5.10.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.4.tar.gz.asc     && tar -xf crate-5.10.4.tar.gz -C /crate --strip-components=1     && rm crate-5.10.4.tar.gz # buildkit
# Mon, 07 Apr 2025 13:02:24 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 07 Apr 2025 13:02:24 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 13:02:24 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 07 Apr 2025 13:02:24 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 07 Apr 2025 13:02:24 GMT
VOLUME [/data]
# Mon, 07 Apr 2025 13:02:24 GMT
WORKDIR /data
# Mon, 07 Apr 2025 13:02:24 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 07 Apr 2025 13:02:24 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 07 Apr 2025 13:02:24 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 07 Apr 2025 13:02:24 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-04-07T13:02:24.481728 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.4
# Mon, 07 Apr 2025 13:02:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Apr 2025 13:02:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 13:02:24 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:a3fe057ad103398a19e5279ad7d72ce89b6fe2cafdc6602093481d014edc3819`  
		Last Modified: Mon, 14 Apr 2025 21:04:12 GMT  
		Size: 66.7 MB (66703326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e0ec4e85910e88ae5693be014495ddfcfb4d475413e9445da83be4324d13ba`  
		Last Modified: Mon, 14 Apr 2025 21:08:03 GMT  
		Size: 15.4 MB (15404567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb68b039267d216928d8f470bab57d8012f1c48ed2ee62889f652d749139d498`  
		Last Modified: Mon, 14 Apr 2025 21:08:05 GMT  
		Size: 149.7 MB (149661079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206ded9a16680ed8662e12fb43d974b450e6627387db1f6f79397fc17c318fa3`  
		Last Modified: Mon, 14 Apr 2025 21:08:03 GMT  
		Size: 1.9 MB (1943631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c0876332de2d3cfda56b7110f93963d12ea24d04d604a549ba92950b2cfb00`  
		Last Modified: Mon, 14 Apr 2025 21:08:03 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1beb8adcd8fa5e9ec7a21a9d70e117d16c8246f6a5e6c9c08eed4940b53992aa`  
		Last Modified: Mon, 14 Apr 2025 21:08:04 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2088c0fa8e3ae16ed456ed52417639e717ea1becebe8eaba76d7608052ed7bf`  
		Last Modified: Mon, 14 Apr 2025 21:08:04 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d5fde7835c372320167f48ba6385f315385a37075ff26a0a97c8eb040529bc`  
		Last Modified: Mon, 14 Apr 2025 21:08:04 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:dfeefc048ba73a506973cf4fb5719a53876e859edc93515c5ddf1f4e255e6bde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5192575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdea4f9bdeb1c8bdff78ff63d659f155a2194328658838a8f8b6ad7bf9ac1eff`

```dockerfile
```

-	Layers:
	-	`sha256:3d8c87f1a34eb1ea8be9b7a03256535710392c52ef7bc5f908eb6cd53dd96ae3`  
		Last Modified: Mon, 14 Apr 2025 21:08:03 GMT  
		Size: 5.2 MB (5169375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:089b961f9192e09d23d7373bd2ceb12c727e948ba90ef7882d8d2d9dcbd35474`  
		Last Modified: Mon, 14 Apr 2025 21:08:03 GMT  
		Size: 23.2 KB (23200 bytes)  
		MIME: application/vnd.in-toto+json

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:3097bcc5574fdc845ab8c22af2279cabadaa76ae55a2d43603f77687fa098975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232993387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ea2e63d0e02be53561ded6f060ebf3936e0c7cb78b4cbfd1d7b95c43411eb5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 07 Apr 2025 13:02:24 GMT
ADD almalinux-10-kitten-default-arm64.tar.xz / # buildkit
# Mon, 07 Apr 2025 13:02:24 GMT
CMD ["/bin/bash"]
# Mon, 07 Apr 2025 13:02:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar util-linux gnupg     && dnf clean all     && rm -rf /var/cache/yum # buildkit
# Mon, 07 Apr 2025 13:02:24 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.10.4.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.10.4.tar.gz.asc crate-5.10.4.tar.gz     && rm -rf "$GNUPGHOME" crate-5.10.4.tar.gz.asc     && tar -xf crate-5.10.4.tar.gz -C /crate --strip-components=1     && rm crate-5.10.4.tar.gz # buildkit
# Mon, 07 Apr 2025 13:02:24 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.5.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.5.asc crash_standalone_0.31.5     && rm -rf "$GNUPGHOME" crash_standalone_0.31.5.asc     && mv crash_standalone_0.31.5 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash # buildkit
# Mon, 07 Apr 2025 13:02:24 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 13:02:24 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 07 Apr 2025 13:02:24 GMT
RUN mkdir -p /data/data /data/log # buildkit
# Mon, 07 Apr 2025 13:02:24 GMT
VOLUME [/data]
# Mon, 07 Apr 2025 13:02:24 GMT
WORKDIR /data
# Mon, 07 Apr 2025 13:02:24 GMT
EXPOSE map[4200/tcp:{} 4300/tcp:{} 5432/tcp:{}]
# Mon, 07 Apr 2025 13:02:24 GMT
COPY --chown=1000:0 config/crate.yml /crate/config/crate.yml # buildkit
# Mon, 07 Apr 2025 13:02:24 GMT
COPY --chown=1000:0 config/log4j2.properties /crate/config/log4j2.properties # buildkit
# Mon, 07 Apr 2025 13:02:24 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2025-04-07T13:02:24.481728 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.10.4
# Mon, 07 Apr 2025 13:02:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Apr 2025 13:02:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 13:02:24 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:443342f58da70c4d8462137201b4af95fe44752374fc07fa7f48092fcf802c88`  
		Last Modified: Mon, 14 Apr 2025 21:03:41 GMT  
		Size: 65.2 MB (65245289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174a192bbbdb738a0ab32cb314abdd2dc66239fe7bb1be4022e0a269ef6131f2`  
		Last Modified: Mon, 14 Apr 2025 21:08:02 GMT  
		Size: 15.5 MB (15465210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc7d1decbd1df988122ca4c85068fd891fb73bea4909c571600cd357a2a667e`  
		Last Modified: Mon, 14 Apr 2025 21:08:07 GMT  
		Size: 150.3 MB (150337372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce7acc7e87cb19c1d3ceaf625fc1c6b777ce40f2714bf69362a183c3313dca0`  
		Last Modified: Mon, 14 Apr 2025 21:08:02 GMT  
		Size: 1.9 MB (1943638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dbe8d0c630dfb805c9811c857a338a93de5de42f5962fe80ea12325dd45258a`  
		Last Modified: Mon, 14 Apr 2025 21:08:02 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff573f00ba40b5fc1eb24052e0c0e257dc62bb57a3724cfdf07fc1ae5c210db`  
		Last Modified: Mon, 14 Apr 2025 21:08:03 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138f2b97cc07c8af616136e8d1e8d58366ac43d8078ded85b63623bd4fc1f976`  
		Last Modified: Mon, 14 Apr 2025 21:08:03 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ec8cb1b52f832401db024039718321c05e1cbb7802aa8db65660548682f119`  
		Last Modified: Mon, 14 Apr 2025 21:08:03 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `crate:latest` - unknown; unknown

```console
$ docker pull crate@sha256:c81866383522b7781484f6c60fc38a84a5332e7bff9160d51d3a9c55b753ab4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7870e0a06cbea8842ff48b582ecf29a75b41c14847bbae355621317f47ff6cdb`

```dockerfile
```

-	Layers:
	-	`sha256:ae5aa980d963eec3d20ba72a556265686279d59c634c3324c25ca370ff967e8a`  
		Last Modified: Mon, 14 Apr 2025 21:08:02 GMT  
		Size: 5.2 MB (5166683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:655b6fac11315b4ced84bb93d68c4964da086d4c04aab5a6fc1a5be4e52f82c5`  
		Last Modified: Mon, 14 Apr 2025 21:08:01 GMT  
		Size: 23.3 KB (23338 bytes)  
		MIME: application/vnd.in-toto+json
