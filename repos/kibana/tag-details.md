<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:6.8.13`](#kibana6813)
-	[`kibana:7.10.1`](#kibana7101)

## `kibana:6.8.13`

```console
$ docker pull kibana@sha256:664b53e52c4a740733a960fc36dfacc3eca0356c00a2562614d11e77bdf8fed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kibana:6.8.13` - linux; amd64

```console
$ docker pull kibana@sha256:ef973ad68e16d5d20825b6219841f60474102a6798d36ecb798c3caa64c625ad
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.6 MB (275616109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:976584caff9c0916546e1ff5f3162ec50797c6ec827a08bf42413770dfea013f`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 10 Aug 2020 18:20:08 GMT
ADD file:61908381d3142ffba798ae9a904476d19b197ab79d0338f14bec0f76649df8d4 in / 
# Mon, 10 Aug 2020 18:20:09 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200809 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-08-09 00:00:00+01:00
# Mon, 10 Aug 2020 18:20:09 GMT
CMD ["/bin/bash"]
# Fri, 16 Oct 2020 10:02:15 GMT
EXPOSE 5601
# Fri, 16 Oct 2020 10:02:31 GMT
RUN yum update -y && yum install -y fontconfig freetype && yum clean all
# Fri, 16 Oct 2020 10:03:19 GMT
COPY --chown=1000:0dir:1db8153f112957995e194ba84e577b87285567ba1110808d7a5157f1cb553cda in /usr/share/kibana 
# Fri, 16 Oct 2020 10:03:20 GMT
WORKDIR /usr/share/kibana
# Fri, 16 Oct 2020 10:03:22 GMT
RUN ln -s /usr/share/kibana /opt/kibana
# Fri, 16 Oct 2020 10:03:23 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 16 Oct 2020 10:03:23 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Oct 2020 10:03:24 GMT
COPY --chown=1000:0file:60b6181f28c99b362092ea6139b6d4112ddd0bef32d52563c33b26bdc2b51318 in /usr/share/kibana/config/kibana.yml 
# Fri, 16 Oct 2020 10:03:25 GMT
COPY --chown=1000:0file:7d472d1939e23e2f10e7c5fd1e9166eefd646214aa0d8a1c09d92af71c9cbd87 in /usr/local/bin/ 
# Fri, 16 Oct 2020 10:03:27 GMT
RUN chmod g+ws /usr/share/kibana && find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \;
# Fri, 16 Oct 2020 10:03:29 GMT
RUN groupadd --gid 1000 kibana && useradd --uid 1000 --gid 1000 --home-dir /usr/share/kibana --no-create-home kibana
# Fri, 16 Oct 2020 10:03:30 GMT
USER kibana
# Fri, 16 Oct 2020 10:03:30 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=kibana org.label-schema.version=6.8.13 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.license=Elastic License license=Elastic License
# Fri, 16 Oct 2020 10:03:30 GMT
CMD ["/usr/local/bin/kibana-docker"]
```

-	Layers:
	-	`sha256:75f829a71a1c5277a7abf55495ac8d16759691d980bf1d931795e5eb68a294c0`  
		Last Modified: Mon, 10 Aug 2020 18:21:46 GMT  
		Size: 75.9 MB (75863188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9193f0796d3228b1aebdddec502abb36e1c4682945dd3ea39e7b12cbf574c96`  
		Last Modified: Thu, 22 Oct 2020 13:53:15 GMT  
		Size: 10.0 MB (9978436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a1c2c9cd6b63cb60777886f4eb9b18de595c8772fca04d68338068ceecd83c`  
		Last Modified: Thu, 22 Oct 2020 13:53:37 GMT  
		Size: 189.8 MB (189769734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd8d45a3354f674b52e28daad4f842d32e7222e77153f96b253a14b0992db41`  
		Last Modified: Thu, 22 Oct 2020 13:53:11 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5bb80463c2e9b1c2dcc2b34299adce75d2d2a7ac750665140714eb41c6c76e6`  
		Last Modified: Thu, 22 Oct 2020 13:53:09 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a82b91a17e6b259520e7a4d5445cfe4543bfef2830be83e4ea3f322a6aef79`  
		Last Modified: Thu, 22 Oct 2020 13:53:08 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44ca46e47a5cd112ae3efc1c77f060f8cc11401eff491ff0528583a7250720c5`  
		Last Modified: Thu, 22 Oct 2020 13:53:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ecddc8043d2224708a55d537dfcdcf701dd7c66e9b506d3b887faa691a50d1`  
		Last Modified: Thu, 22 Oct 2020 13:53:06 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kibana:7.10.1`

```console
$ docker pull kibana@sha256:ee434144dd3f8d0f18bff10eda9918cd8e70f8deaaf6a75adf5d0df7f8094169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kibana:7.10.1` - linux; amd64

```console
$ docker pull kibana@sha256:1731793b7f3e453c65ebaf92ec0b55f4029310ba8abae9e04753a4680dd8210b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.3 MB (364270361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e014820ee3ff7dadb62da2160415f5cb2726c363872f5b35f0cf252b8489ef1`
-	Entrypoint: `["\/usr\/local\/bin\/dumb-init","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 10 Aug 2020 18:19:49 GMT
ADD file:538afc0c5c964ce0dde0141953a4dcf03c2d993c5989c92e7fee418e9305e2a3 in / 
# Mon, 10 Aug 2020 18:19:49 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200809
# Mon, 10 Aug 2020 18:19:49 GMT
CMD ["/bin/bash"]
# Sat, 05 Dec 2020 02:07:22 GMT
EXPOSE 5601
# Sat, 05 Dec 2020 02:07:57 GMT
RUN for iter in {1..10}; do       yum update --setopt=tsflags=nodocs -y &&       yum install --setopt=tsflags=nodocs -y         fontconfig freetype shadow-utils libnss3.so  &&       yum clean all && exit_code=0 && break || exit_code=$? && echo "yum error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code)
# Sat, 05 Dec 2020 02:07:59 GMT
RUN curl -L -o /usr/local/bin/dumb-init https://github.com/Yelp/dumb-init/releases/download/v1.2.2/dumb-init_1.2.2_amd64
# Sat, 05 Dec 2020 02:08:02 GMT
RUN echo "37f2c1f0372a45554f1b89924fbb134fc24c3756efaedf11e07f599494e0eff9  /usr/local/bin/dumb-init" | sha256sum -c -
# Sat, 05 Dec 2020 02:08:04 GMT
RUN chmod +x /usr/local/bin/dumb-init
# Sat, 05 Dec 2020 02:08:06 GMT
RUN mkdir /usr/share/fonts/local
# Sat, 05 Dec 2020 02:08:12 GMT
RUN curl -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc
# Sat, 05 Dec 2020 02:08:15 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c -
# Sat, 05 Dec 2020 02:08:18 GMT
RUN fc-cache -v
# Sat, 05 Dec 2020 02:09:01 GMT
COPY --chown=1000:0dir:88ff5f213775dcdf96460510190bcb33f7b871b8212a0ce21bfb38585afa4dd7 in /usr/share/kibana 
# Sat, 05 Dec 2020 02:09:02 GMT
WORKDIR /usr/share/kibana
# Sat, 05 Dec 2020 02:09:04 GMT
RUN ln -s /usr/share/kibana /opt/kibana
# Sat, 05 Dec 2020 02:09:04 GMT
ENV ELASTIC_CONTAINER=true
# Sat, 05 Dec 2020 02:09:04 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Dec 2020 02:09:05 GMT
COPY --chown=1000:0file:ea1f294356f14dfc1a50e3303613e69f187589962058569d5b3282460d7f28cb in /usr/share/kibana/config/kibana.yml 
# Sat, 05 Dec 2020 02:09:05 GMT
COPY --chown=1000:0file:4ade66f18eade4e7231bbe0e262fbc0586d4707c4c733be1134a1556ab326c47 in /usr/local/bin/ 
# Sat, 05 Dec 2020 02:09:08 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \;
# Sat, 05 Dec 2020 02:09:10 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} +
# Sat, 05 Dec 2020 02:09:12 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000       --home-dir /usr/share/kibana --no-create-home       kibana
# Sat, 05 Dec 2020 02:09:13 GMT
LABEL org.label-schema.build-date=2020-12-05T02:04:38.350Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=608c5e5dd32659e8afadd520d0cdc58766ba505b org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.10.1 org.opencontainers.image.created=2020-12-05T02:04:38.350Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=608c5e5dd32659e8afadd520d0cdc58766ba505b org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.10.1
# Sat, 05 Dec 2020 02:09:13 GMT
USER kibana
# Sat, 05 Dec 2020 02:09:14 GMT
ENTRYPOINT ["/usr/local/bin/dumb-init" "--"]
# Sat, 05 Dec 2020 02:09:14 GMT
CMD ["/usr/local/bin/kibana-docker"]
```

-	Layers:
	-	`sha256:3c72a8ed68140139e483fe7368ae4d9651422749e91483557cbd5ecf99a96110`  
		Last Modified: Mon, 10 Aug 2020 18:21:27 GMT  
		Size: 74.9 MB (74868121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b131d31acbf41fc3622c9dc3c77ef2686f7e62029c3b4a91351088029a95a2`  
		Last Modified: Wed, 09 Dec 2020 15:09:37 GMT  
		Size: 22.5 MB (22468463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d3f5b808208dbbab4d14369c618f4eb98fec9af3c625a3cafa32812c012069`  
		Last Modified: Wed, 09 Dec 2020 15:09:05 GMT  
		Size: 30.2 KB (30198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce01809aac54eca314c194fefdba77114571547011f3f1d33be06da4769ac867`  
		Last Modified: Wed, 09 Dec 2020 15:09:04 GMT  
		Size: 30.2 KB (30194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd62ae8b256072881da718287c4a4fc909ba9adfd457b80afbab20d48ec90077`  
		Last Modified: Wed, 09 Dec 2020 15:09:01 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1b4e9139443327f35616c0ffbc2095e268ccee4b479fe86462a862585fb6e5`  
		Last Modified: Wed, 09 Dec 2020 15:09:25 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a14f0f39a44441e8182c900ef50f6ee4ccb8e596f6ebf6042f5fd499b6c67b19`  
		Last Modified: Wed, 09 Dec 2020 15:09:00 GMT  
		Size: 8.3 KB (8317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b9eac14d916ffdfd17ba492da20122ff84bfedbd7cd5baef1f9cb1eb974366d`  
		Last Modified: Wed, 09 Dec 2020 15:50:55 GMT  
		Size: 250.2 MB (250202495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d309d052637ad339984ca3a6ce477a0de7bf83648abde690622d117bd2eddaa`  
		Last Modified: Wed, 09 Dec 2020 15:50:16 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35a5bce98d226cdeb2d6b365926bcfcc100a43aa83787c364c85e5ade179b03`  
		Last Modified: Wed, 09 Dec 2020 15:50:15 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57619633b3746d7c027dafccc04c8be67c31131299cd2c0ace6d6f45bf3b851`  
		Last Modified: Wed, 09 Dec 2020 15:50:14 GMT  
		Size: 3.1 KB (3133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c6a30a64805d0c218ec47f621f47f7d0db0ec7c30c7f632a275d2cbebafbdb`  
		Last Modified: Wed, 09 Dec 2020 15:50:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bff97a8e672373ecc951721c6dc1d0cbf7a4938dedc92d16ade16a3dd5efdbd`  
		Last Modified: Wed, 09 Dec 2020 15:08:56 GMT  
		Size: 196.4 KB (196361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ffe1970589ad26389e35f885461fab44fc0e9cf3cd12e3ebbe622158bded92c`  
		Last Modified: Wed, 09 Dec 2020 15:50:10 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
