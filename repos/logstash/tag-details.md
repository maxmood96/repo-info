<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:8.19.12`](#logstash81912)
-	[`logstash:9.2.6`](#logstash926)
-	[`logstash:9.3.1`](#logstash931)

## `logstash:8.19.12`

```console
$ docker pull logstash@sha256:06b919ac6014d7851f79ec63e2c71ccc7c4f2997dcf536ada2d8d0baffa338bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.19.12` - linux; amd64

```console
$ docker pull logstash@sha256:dcde08c021533c70f83d4440c9174e218b6ec674eb57f31f7740555d45656bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **534.5 MB (534503071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875fba3fd9f22f6f69e58b45b453f3b116b57af712c62b6b1010ea9167f57e9f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Thu, 26 Feb 2026 19:04:16 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 26 Feb 2026 19:04:16 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 26 Feb 2026 19:14:24 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.12-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.12 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 26 Feb 2026 19:14:24 GMT
WORKDIR /usr/share/logstash
# Thu, 26 Feb 2026 19:14:24 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 26 Feb 2026 19:14:24 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 19:14:24 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 26 Feb 2026 19:14:24 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 26 Feb 2026 19:14:24 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 26 Feb 2026 19:14:24 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 26 Feb 2026 19:14:24 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 26 Feb 2026 19:14:24 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Thu, 26 Feb 2026 19:14:24 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Thu, 26 Feb 2026 19:14:24 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 26 Feb 2026 19:14:24 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:14:24 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 26 Feb 2026 19:14:24 GMT
USER 1000
# Thu, 26 Feb 2026 19:14:24 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 26 Feb 2026 19:14:24 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.12 org.opencontainers.image.version=8.19.12 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2026-02-18T12:09:10+00:00 org.opencontainers.image.created=2026-02-18T12:09:10+00:00
# Thu, 26 Feb 2026 19:14:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff33bca73127d6aefee757e13944f4a8733820fd4272f7e9a65112548f7d3653`  
		Last Modified: Thu, 26 Feb 2026 19:15:03 GMT  
		Size: 53.2 MB (53152586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04dc2d4692036cca0c24c348a84442e90bee30b5490b69a8b6c746c2e3c4ebb8`  
		Last Modified: Thu, 26 Feb 2026 19:15:00 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46e7b783ad4d3375249ba6bf6218e346a03fb5350a68a056ff75f6a609e9812`  
		Last Modified: Thu, 26 Feb 2026 19:15:11 GMT  
		Size: 451.4 MB (451355145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e241109f837eef03c46ea5d45e6a1e6e12e2e9cd0d01551476a0a08cb2e6cc`  
		Last Modified: Thu, 26 Feb 2026 19:15:01 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d80a97704fb72a2d9582cd8be5710c5a0c4a2ff4ca9bf591780c1780fb6b953`  
		Last Modified: Thu, 26 Feb 2026 19:15:02 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f16300b068ed0ce2560678adf6b9bb0cf7916f02188e4ba7680d18d863650b4`  
		Last Modified: Thu, 26 Feb 2026 19:15:02 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3dbe59c3f60fa3b9ae8bad866a8b093b67d3eaaa9b14994a010f303e524610`  
		Last Modified: Thu, 26 Feb 2026 19:15:03 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587e6efd0f049388df98bef878730c2ec809b7e345e40b6663462af0d70876fe`  
		Last Modified: Thu, 26 Feb 2026 19:15:03 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b425f6879e23d03e1caa22916b6e8a42bfb4819b17a4ddf63547451f820bc79f`  
		Last Modified: Thu, 26 Feb 2026 19:15:04 GMT  
		Size: 255.2 KB (255183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5e58dd6e9a6fe902408b97fa1b78370b3a9b2d1e0880e3f59591779867c235`  
		Last Modified: Thu, 26 Feb 2026 19:15:04 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce31ef92721f83e428e05b8b18786925ccdc2fef494fc04dc04ff95f8bef8117`  
		Last Modified: Thu, 26 Feb 2026 19:15:04 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.12` - unknown; unknown

```console
$ docker pull logstash@sha256:4869129679cab3eab1f51e2cea9ddce9a0798a5bf9bd871f15dd87bbbefe12e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3720981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3267c1448478bb347045fcc57c9d2b36c66b5d57e990014800c2457c749947`

```dockerfile
```

-	Layers:
	-	`sha256:ad06b8dcd8e3111c11d63e69fc90d1bdbb6c679612f13b12d35f80940c0fd839`  
		Last Modified: Thu, 26 Feb 2026 19:15:01 GMT  
		Size: 3.7 MB (3685136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:211d10ff07458118212294a424719fcb0c3f84200a1b0767b362306879492e9f`  
		Last Modified: Thu, 26 Feb 2026 19:15:00 GMT  
		Size: 35.8 KB (35845 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.19.12` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:c0ff002b9d8ee677dfee2cfd241dcfc2e4cda9f87350ff4105f8a20a94dd57e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **534.5 MB (534528619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f0cee604490e0488e98be69656cf6ac3867fb127912f9dfff29d69fc92b973`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Thu, 26 Feb 2026 19:03:30 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 26 Feb 2026 19:03:30 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 26 Feb 2026 19:12:02 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.12-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.12 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 26 Feb 2026 19:12:02 GMT
WORKDIR /usr/share/logstash
# Thu, 26 Feb 2026 19:12:02 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 26 Feb 2026 19:12:02 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 19:12:02 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 26 Feb 2026 19:12:02 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 26 Feb 2026 19:12:02 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 26 Feb 2026 19:12:02 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 26 Feb 2026 19:12:02 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 26 Feb 2026 19:12:02 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Thu, 26 Feb 2026 19:12:02 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Thu, 26 Feb 2026 19:12:02 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 26 Feb 2026 19:12:02 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:12:02 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 26 Feb 2026 19:12:02 GMT
USER 1000
# Thu, 26 Feb 2026 19:12:02 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 26 Feb 2026 19:12:02 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.12 org.opencontainers.image.version=8.19.12 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2026-02-18T12:09:10+00:00 org.opencontainers.image.created=2026-02-18T12:09:10+00:00
# Thu, 26 Feb 2026 19:12:02 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05036f2cb1dde1c802160d0a7c786c3e59ab9989a3e87cd4c3194784adb6dd6`  
		Last Modified: Thu, 26 Feb 2026 19:12:43 GMT  
		Size: 55.8 MB (55757400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c63a1b2a599edde60c13f55664387a704f0c9b98bad394eabece4e670c71de0`  
		Last Modified: Thu, 26 Feb 2026 19:12:41 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1a4a39fcb179ccf9072d82105d18e3a704bf013fd470323933a39f5b2b5c19`  
		Last Modified: Thu, 26 Feb 2026 19:12:51 GMT  
		Size: 449.6 MB (449638374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7577243f25a36de53e7541a96057f3369e13f929d3e48abbfcd435c72bf21de1`  
		Last Modified: Thu, 26 Feb 2026 19:12:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2eb9fcbb26b14bd5dbfe3baa3082789168a3b759fcdbf29f72c446b925e9b05`  
		Last Modified: Thu, 26 Feb 2026 19:12:42 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3cbae63eb670421bdc3bd4443145b5046f40bb5e01a86076cdcd5d7f48ce694`  
		Last Modified: Thu, 26 Feb 2026 19:12:43 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0992eb5aca6e452b10e533a572febac566e1644f4e49c1c9f1f9b15b557f62ed`  
		Last Modified: Thu, 26 Feb 2026 19:12:43 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e20491c9f2988e77f6447b2f48abfa8f3859da2fe50b94fbc861f86818afae`  
		Last Modified: Thu, 26 Feb 2026 19:12:44 GMT  
		Size: 6.3 KB (6294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c74bffa3d74739e09a145acc230dad0af23eaaa3eafc1656f55624e98df7525`  
		Last Modified: Thu, 26 Feb 2026 19:12:45 GMT  
		Size: 255.2 KB (255185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76de5fcccd375cc7c37dde808c3f074614275d1a8bb9fec7fba7b9e9b526e4a4`  
		Last Modified: Thu, 26 Feb 2026 19:12:45 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d114d036716888fab790829eb6cd918f4fb29f1f678d5c893128d18285baafb2`  
		Last Modified: Thu, 26 Feb 2026 19:12:45 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.12` - unknown; unknown

```console
$ docker pull logstash@sha256:90ef245ec88ec2b65d2ef66adf85f208473b933857e7ee55d98d8d2a00a213d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3721534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7fa283a13754405238d4bdcd1b6edccb58e0f1f42b1b25378ebc1d83642c103`

```dockerfile
```

-	Layers:
	-	`sha256:dbd7044cecb3cd34e9782432163b0da793067ae4ed6f29b02349175e31ccd0be`  
		Last Modified: Thu, 26 Feb 2026 19:12:41 GMT  
		Size: 3.7 MB (3685561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c1cfdcf03cea9f6cc20e9fcef1acb8db214f7dbbce998cdb10a03bf0762230a`  
		Last Modified: Thu, 26 Feb 2026 19:12:41 GMT  
		Size: 36.0 KB (35973 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.2.6`

```console
$ docker pull logstash@sha256:76c90d66fade4a1419d8d4474b9bc5a2961d4ee40ca055579fdf2c15d1e71e3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.2.6` - linux; amd64

```console
$ docker pull logstash@sha256:7fb4bef0b99e2cb52b37bc1d15c6b33845643ef9d0d31019c024444b100af2f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **496.1 MB (496125058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8be8f39df596e45d84941f6d128e88e593e7e88667ed80d7d0874fe54d00f0f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 16:42:45 GMT
ENV container oci
# Tue, 17 Feb 2026 16:42:46 GMT
COPY dir:a84da6f36b88f4eb0d6c411f65b34c1a9d85150d3035dd516db4ece0c2569465 in /      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 16:42:46 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:6326b4becf4dcc53eab9a0e80efe304ada5421165d0586862d969cb5fa826bd8 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:6326b4becf4dcc53eab9a0e80efe304ada5421165d0586862d969cb5fa826bd8 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:42:46 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T16:42:34Z" "org.opencontainers.image.created"="2026-02-17T16:42:34Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T16:42:34Z
# Thu, 26 Feb 2026 19:04:06 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 26 Feb 2026 19:04:06 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 19:04:06 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 26 Feb 2026 19:04:06 GMT
WORKDIR /usr/share
# Thu, 26 Feb 2026 19:04:08 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 26 Feb 2026 19:14:05 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.6-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.6 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 26 Feb 2026 19:14:05 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Thu, 26 Feb 2026 19:14:05 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Thu, 26 Feb 2026 19:14:06 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 26 Feb 2026 19:14:06 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 26 Feb 2026 19:14:06 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 26 Feb 2026 19:14:06 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 26 Feb 2026 19:14:06 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:14:06 GMT
WORKDIR /usr/share/logstash
# Thu, 26 Feb 2026 19:14:06 GMT
USER 1000
# Thu, 26 Feb 2026 19:14:06 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 26 Feb 2026 19:14:06 GMT
LABEL org.label-schema.build-date=2026-02-18T12:05:35+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.6 org.opencontainers.image.created=2026-02-18T12:05:35+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.6 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 26 Feb 2026 19:14:06 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:4638e3415987f378f2d6dd70f9c6a2869dd5ebd09e3510ba45e46bbb6ec1a3dd`  
		Last Modified: Tue, 17 Feb 2026 18:08:54 GMT  
		Size: 40.0 MB (40033596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de18382bb01a4961b871d8b29c3b0318b3928c73c4c0a50861287594fe632c2`  
		Last Modified: Thu, 26 Feb 2026 19:14:39 GMT  
		Size: 5.2 MB (5157506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7d091e95c81ad295a3fb975344acbb671a61ab2a566f9077b20abb82293873`  
		Last Modified: Thu, 26 Feb 2026 19:14:47 GMT  
		Size: 450.7 MB (450669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878d30ffe43a843fb1bea39e07502ac5ceecaee29630c0abb722bccdaf950658`  
		Last Modified: Thu, 26 Feb 2026 19:14:39 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de934c1f5ad0152e7ce0891f528bc13c3803c68d45477606f052af4e2cbf8a1`  
		Last Modified: Thu, 26 Feb 2026 19:14:39 GMT  
		Size: 255.2 KB (255185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371edc9e15197c75d4b21d702498879ab0fbcd087bf0a804c75f09fd3f218d07`  
		Last Modified: Thu, 26 Feb 2026 19:14:40 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e85a9e9bdc19e9a3abec270d6cfbcf3ed766c13e26e17cce02d79235bd3478`  
		Last Modified: Thu, 26 Feb 2026 19:14:40 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb3557a6604fdbc1c112c114b34865dafef2f634a0f13b5379e5da4935a3b4a`  
		Last Modified: Thu, 26 Feb 2026 19:14:40 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff2d21a21a5b3a9735c3e5634a5d217e66a5fef5b8a024ba91ad9f75061016f`  
		Last Modified: Thu, 26 Feb 2026 19:14:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ef5572c960faaab60a1b61c567e33f1d77dc47f107f090a0c6409a7f575d5c`  
		Last Modified: Thu, 26 Feb 2026 19:14:41 GMT  
		Size: 708.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.6` - unknown; unknown

```console
$ docker pull logstash@sha256:fe8627f344c3ab6c77cbdd265a4b61170a0606ff107e7724115f9358dc7cdefc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2163307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:477b546f700ea9ad1e8626a5836c93c7c394f38e34e0ce1e1825d6253f3f197e`

```dockerfile
```

-	Layers:
	-	`sha256:ca9fba71340b22320cf485cfda33671bebfcb5d712e7b4f96c7d05b2a86d84dd`  
		Last Modified: Thu, 26 Feb 2026 19:14:39 GMT  
		Size: 2.1 MB (2133107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d178302c4f713dc713f87017c62d27369d03cf96f1057a5da30e6356be457ed0`  
		Last Modified: Thu, 26 Feb 2026 19:14:39 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.2.6` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:fe20a4ae581ef7dac6e45a31c69a2955b7eae648ab7cc808af3b1b7ccc3f450f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.6 MB (492568536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade4a0268475f7f96c99e9ac321dc7241466eb20d9901605fd05c35070b9778d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 16:45:44 GMT
ENV container oci
# Tue, 17 Feb 2026 16:45:45 GMT
COPY dir:ac0ab1292a52ccb276077ed994531e1a3deef7d271c3502d95032264a0448d19 in /      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 16:45:45 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:b6e9611fd18f4ab100ec73ea6037b1118108a414096af83dfb78d47ad0a2b249 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:b6e9611fd18f4ab100ec73ea6037b1118108a414096af83dfb78d47ad0a2b249 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:45:46 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T16:45:31Z" "org.opencontainers.image.created"="2026-02-17T16:45:31Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T16:45:31Z
# Thu, 26 Feb 2026 19:03:16 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 26 Feb 2026 19:03:16 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 19:03:16 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 26 Feb 2026 19:03:16 GMT
WORKDIR /usr/share
# Thu, 26 Feb 2026 19:03:18 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 26 Feb 2026 19:15:21 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.6-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.6 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 26 Feb 2026 19:15:21 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Thu, 26 Feb 2026 19:15:21 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Thu, 26 Feb 2026 19:15:21 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 26 Feb 2026 19:15:22 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 26 Feb 2026 19:15:22 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 26 Feb 2026 19:15:22 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 26 Feb 2026 19:15:22 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:15:22 GMT
WORKDIR /usr/share/logstash
# Thu, 26 Feb 2026 19:15:22 GMT
USER 1000
# Thu, 26 Feb 2026 19:15:22 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 26 Feb 2026 19:15:22 GMT
LABEL org.label-schema.build-date=2026-02-18T12:05:35+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.6 org.opencontainers.image.created=2026-02-18T12:05:35+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.6 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 26 Feb 2026 19:15:22 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:063fbd5fac6af91f4042bbe66bae69795aa46675d5b0c800ed195ad79ed8fb02`  
		Last Modified: Tue, 17 Feb 2026 18:09:11 GMT  
		Size: 38.2 MB (38202534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac09051e4d456e888c0fbd9fe38726ef7ecfab9133f32602e41478ccbffb4e6`  
		Last Modified: Thu, 26 Feb 2026 19:15:59 GMT  
		Size: 5.2 MB (5155552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c8409cc2ffd2d5a5695d8130d8ec18684006f18586a9564225762a9a077bc2`  
		Last Modified: Thu, 26 Feb 2026 19:16:13 GMT  
		Size: 448.9 MB (448945708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c265a9fa1fbfdd0b5f531bbe7197ae8b4992e0d5ec939dc33b6f444412886046`  
		Last Modified: Thu, 26 Feb 2026 19:15:59 GMT  
		Size: 6.3 KB (6293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc57e0d1eda46ebbdb303e777751293c0761ce0f6ee1e3a29abe97cd6e95b88`  
		Last Modified: Thu, 26 Feb 2026 19:15:59 GMT  
		Size: 255.2 KB (255181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c18b4715fe34414fbecf1f64ced82f5f73e1f8405e49ed7e8fb0c0ac966e45`  
		Last Modified: Thu, 26 Feb 2026 19:16:00 GMT  
		Size: 352.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dcaa1df89e8e85bb48451e94b096fe9225a2d77072b72e4c230000064a5cfe7`  
		Last Modified: Thu, 26 Feb 2026 19:16:00 GMT  
		Size: 1.6 KB (1582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e198bcbc93a035399d497dc263afa507bebad95bb8b7de2a8ce001fe44ce3232`  
		Last Modified: Thu, 26 Feb 2026 19:16:01 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d09ad2e36206b7ee6f08dbc90b061a166da09d1387907f3e32858c12e65ccc`  
		Last Modified: Thu, 26 Feb 2026 19:16:01 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb219eeac2fb47d73e4cd7bf729c0f905add264832d4a6ee2e508a9b5efc665`  
		Last Modified: Thu, 26 Feb 2026 19:16:02 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.6` - unknown; unknown

```console
$ docker pull logstash@sha256:d64358c21ae7fb15f8c42e49ecee20a0074e61ca63c1b369c6c49d5389acc1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2163954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0328555917d2422c5aad6d6c0db7f5544cc2b7aa34c815736688924e60d98f8e`

```dockerfile
```

-	Layers:
	-	`sha256:f3f6094452e177e7f9c69e7e92b80e3746c25d39a062e132071b4d2bb4a17c45`  
		Last Modified: Thu, 26 Feb 2026 19:15:59 GMT  
		Size: 2.1 MB (2133677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82b15cab744989a883740631acf5f48ea04d5b15d31dcdc2b7416498820a57f7`  
		Last Modified: Thu, 26 Feb 2026 19:15:59 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.3.1`

```console
$ docker pull logstash@sha256:d804f4994cebd9002e33a6f0b561dd3a15108222045f5d182da3c2675f26d177
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.3.1` - linux; amd64

```console
$ docker pull logstash@sha256:6c8a61daa50fc3d4aabd1856966e908d76cea3d342fa7fed820ff11660ca3b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.5 MB (511544593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93d37883208d62d73d599c22e1ef89b21a09151f966905096028325945d57a2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 16:42:45 GMT
ENV container oci
# Tue, 17 Feb 2026 16:42:46 GMT
COPY dir:a84da6f36b88f4eb0d6c411f65b34c1a9d85150d3035dd516db4ece0c2569465 in /      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 16:42:46 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:6326b4becf4dcc53eab9a0e80efe304ada5421165d0586862d969cb5fa826bd8 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:6326b4becf4dcc53eab9a0e80efe304ada5421165d0586862d969cb5fa826bd8 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:42:46 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T16:42:34Z" "org.opencontainers.image.created"="2026-02-17T16:42:34Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T16:42:34Z
# Thu, 26 Feb 2026 19:04:48 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 26 Feb 2026 19:04:48 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 19:04:48 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 26 Feb 2026 19:04:48 GMT
WORKDIR /usr/share
# Thu, 26 Feb 2026 19:04:50 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 26 Feb 2026 19:13:38 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.1-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.1 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 26 Feb 2026 19:13:38 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Thu, 26 Feb 2026 19:13:38 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Thu, 26 Feb 2026 19:13:38 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 26 Feb 2026 19:13:39 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 26 Feb 2026 19:13:39 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 26 Feb 2026 19:13:39 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 26 Feb 2026 19:13:39 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:13:39 GMT
WORKDIR /usr/share/logstash
# Thu, 26 Feb 2026 19:13:39 GMT
USER 1000
# Thu, 26 Feb 2026 19:13:39 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 26 Feb 2026 19:13:39 GMT
LABEL org.label-schema.build-date=2026-02-18T12:06:22+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.1 org.opencontainers.image.created=2026-02-18T12:06:22+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.1 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 26 Feb 2026 19:13:39 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:4638e3415987f378f2d6dd70f9c6a2869dd5ebd09e3510ba45e46bbb6ec1a3dd`  
		Last Modified: Tue, 17 Feb 2026 18:08:54 GMT  
		Size: 40.0 MB (40033596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b365c427323344bce1f8aa0a4dcb56e521fe2ddce6ba9344bcc2c56837e7cd77`  
		Last Modified: Thu, 26 Feb 2026 19:14:11 GMT  
		Size: 5.2 MB (5157563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168698f1a4876a4c262aae2cd6a4a48060e46262bc4cdf9434202f3a0fb97b2d`  
		Last Modified: Thu, 26 Feb 2026 19:14:20 GMT  
		Size: 466.1 MB (466088686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e823800da80658d1d515a5452d5d981fd09798a9962dafdacebafd6b0917584`  
		Last Modified: Thu, 26 Feb 2026 19:14:11 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365d9df5fdbda4ded608980deede085b54bbd9c0170ce396e0bdda6dedfaef47`  
		Last Modified: Thu, 26 Feb 2026 19:14:11 GMT  
		Size: 255.2 KB (255183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fd85866339f03bc94c01f85b2c64a1b1716ffaf50badd19cc53da3d3e8acc9`  
		Last Modified: Thu, 26 Feb 2026 19:14:12 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7abc90632bdc60cdb5d028d36b6d8cfb6c0a2282d8e8df0bdf7fbe327a2fb0`  
		Last Modified: Thu, 26 Feb 2026 19:14:12 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b776e51240dafcc63adb0904ddbf3619560146810062c1ff6d5a1bc3a43763`  
		Last Modified: Thu, 26 Feb 2026 19:14:12 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48af75da94b8a21cbf385fa102710e3ed99fbae7eff25398c8c3b04503b466dc`  
		Last Modified: Thu, 26 Feb 2026 19:14:13 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925500430a18f6ab72a28376a5377d47c02ff0832b61c2df86cfb4b8203a449c`  
		Last Modified: Thu, 26 Feb 2026 19:14:13 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.1` - unknown; unknown

```console
$ docker pull logstash@sha256:420bcc46f9a71966116258a72cd0825c0bb751d65e0b285427788a3e464dd628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2142266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23c45126cf665d9fb0be70df15f87fef8ce8956b083a67b8b10827fec9c09ee`

```dockerfile
```

-	Layers:
	-	`sha256:a30653000971a86326f31cddb615558868c76ce9a05f162d1c7c3b3a5c0527a5`  
		Last Modified: Thu, 26 Feb 2026 19:14:11 GMT  
		Size: 2.1 MB (2112066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efdea9161f8adf2b98384346f44e50b74d010ad0767be0421e8dcf8309fd5f1b`  
		Last Modified: Thu, 26 Feb 2026 19:14:11 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.3.1` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:bdae0ff89f5a6b7de5c7231a7ff2ce09f29431af2f14df1b0d7feec1bdc41ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **508.0 MB (507985162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303ab2f611f8a37aa96c7cbda7a225e9572c721b8a46474e87137946efd0e668`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 16:45:44 GMT
ENV container oci
# Tue, 17 Feb 2026 16:45:45 GMT
COPY dir:ac0ab1292a52ccb276077ed994531e1a3deef7d271c3502d95032264a0448d19 in /      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 16:45:45 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:b6e9611fd18f4ab100ec73ea6037b1118108a414096af83dfb78d47ad0a2b249 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:b6e9611fd18f4ab100ec73ea6037b1118108a414096af83dfb78d47ad0a2b249 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:45:46 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T16:45:31Z" "org.opencontainers.image.created"="2026-02-17T16:45:31Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T16:45:31Z
# Thu, 26 Feb 2026 19:03:38 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 26 Feb 2026 19:03:38 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 19:03:38 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 26 Feb 2026 19:03:38 GMT
WORKDIR /usr/share
# Thu, 26 Feb 2026 19:03:40 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 26 Feb 2026 19:10:12 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.1-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.1 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 26 Feb 2026 19:10:12 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Thu, 26 Feb 2026 19:10:12 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Thu, 26 Feb 2026 19:10:12 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 26 Feb 2026 19:10:12 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 26 Feb 2026 19:10:12 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 26 Feb 2026 19:10:12 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 26 Feb 2026 19:10:12 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:10:12 GMT
WORKDIR /usr/share/logstash
# Thu, 26 Feb 2026 19:10:12 GMT
USER 1000
# Thu, 26 Feb 2026 19:10:12 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 26 Feb 2026 19:10:12 GMT
LABEL org.label-schema.build-date=2026-02-18T12:06:22+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.1 org.opencontainers.image.created=2026-02-18T12:06:22+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.1 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 26 Feb 2026 19:10:12 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:063fbd5fac6af91f4042bbe66bae69795aa46675d5b0c800ed195ad79ed8fb02`  
		Last Modified: Tue, 17 Feb 2026 18:09:11 GMT  
		Size: 38.2 MB (38202534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4e2d0896afd1c6aac670c3aad65a0b5e6adae6d10052979d44251d0ebe69f5`  
		Last Modified: Thu, 26 Feb 2026 19:10:50 GMT  
		Size: 5.2 MB (5155548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e85445672fb9bfe3a70ef7cb3e721a865499944b842a83e47ddb85425ac9486`  
		Last Modified: Thu, 26 Feb 2026 19:11:01 GMT  
		Size: 464.4 MB (464362329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe0fb378bb8719fb177b10c941038ff27348ef0ba8438dbd164d8f099c8478a`  
		Last Modified: Thu, 26 Feb 2026 19:10:49 GMT  
		Size: 6.3 KB (6299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9be51a153b1c8693ea2412bc33c8750e7a66bf59c284952754960c312a11704`  
		Last Modified: Thu, 26 Feb 2026 19:10:50 GMT  
		Size: 255.2 KB (255189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a36b6555d9b165a2c38687052708a3e16de80878f493e0ea4009273658af7e2`  
		Last Modified: Thu, 26 Feb 2026 19:10:51 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ab8e3a84ac17c40702a8b6870b1ef455a756b2d89094a3f4b6d7dd86a8df46`  
		Last Modified: Thu, 26 Feb 2026 19:10:51 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0350ab7ab3af9d7310bd08c38775ee9af6ebc967781f0fe7d3be7108ecff9fa`  
		Last Modified: Thu, 26 Feb 2026 19:10:51 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aca2a40c929aab468067eaa1d8b42cd81a77ae29d7052ed30d99a552178b077`  
		Last Modified: Thu, 26 Feb 2026 19:10:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af374ba58b292f8bc2852d5dc312304ae68595f81cdbe59ea9778ebdbfc44cae`  
		Last Modified: Thu, 26 Feb 2026 19:10:52 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.1` - unknown; unknown

```console
$ docker pull logstash@sha256:f6c645b34a848040b0d86fc523bf22c1802cd3912eb026f7498f3910493d635a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2142913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d069ec2c409d032c763589587c735b3584d61ed05f0f14da0a2bd2296b7c21e`

```dockerfile
```

-	Layers:
	-	`sha256:7c78ed2f67d9a84bbb9ac7318fcc1a2c049751573dace64cf6987420f2e2be35`  
		Last Modified: Thu, 26 Feb 2026 19:10:50 GMT  
		Size: 2.1 MB (2112636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0436fb31715a88c6a08d8e938cb068562e56b1da15becf2a445a7892f2c09990`  
		Last Modified: Thu, 26 Feb 2026 19:10:49 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json
