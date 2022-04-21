<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:6.8.23`](#kibana6823)
-	[`kibana:7.17.3`](#kibana7173)
-	[`kibana:8.1.3`](#kibana813)

## `kibana:6.8.23`

```console
$ docker pull kibana@sha256:dd123d133fa7e995f83eef23df6aad30c589711e6171fee8db63097a7706eae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kibana:6.8.23` - linux; amd64

```console
$ docker pull kibana@sha256:adb468810c34ccc141f01ea79135d5a2f48d09890ecd08ce59ec94444f0a09f1
```

-	Docker Version: 20.10.10
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.8 MB (325750637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e174261beaec7ef8b8fc7e3df6b62b87e442f3451d408e7fe4525b151a061ebd`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Thu, 06 Jan 2022 22:40:29 GMT
EXPOSE 5601
# Thu, 06 Jan 2022 22:41:30 GMT
RUN yum update -y && yum install -y fontconfig freetype && yum clean all
# Thu, 06 Jan 2022 22:42:25 GMT
COPY --chown=1000:0dir:91d1ac171c4ceb98ce1764191b4bde36072fa18167199a2214eb559670a34b06 in /usr/share/kibana 
# Thu, 06 Jan 2022 22:42:28 GMT
WORKDIR /usr/share/kibana
# Thu, 06 Jan 2022 22:42:29 GMT
RUN ln -s /usr/share/kibana /opt/kibana
# Thu, 06 Jan 2022 22:42:30 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 06 Jan 2022 22:42:30 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jan 2022 22:42:31 GMT
COPY --chown=1000:0file:60b6181f28c99b362092ea6139b6d4112ddd0bef32d52563c33b26bdc2b51318 in /usr/share/kibana/config/kibana.yml 
# Thu, 06 Jan 2022 22:42:31 GMT
COPY --chown=1000:0file:7d472d1939e23e2f10e7c5fd1e9166eefd646214aa0d8a1c09d92af71c9cbd87 in /usr/local/bin/ 
# Thu, 06 Jan 2022 22:42:34 GMT
RUN chmod g+ws /usr/share/kibana && find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \;
# Thu, 06 Jan 2022 22:42:39 GMT
RUN groupadd --gid 1000 kibana && useradd --uid 1000 --gid 1000 --home-dir /usr/share/kibana --no-create-home kibana
# Thu, 06 Jan 2022 22:42:39 GMT
USER kibana
# Thu, 06 Jan 2022 22:42:40 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=kibana org.label-schema.version=6.8.23 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.license=Elastic License license=Elastic License
# Thu, 06 Jan 2022 22:42:41 GMT
CMD ["/usr/local/bin/kibana-docker"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842e4249e10492c4ab35d3e76f93cad922781f7d61752e1b4b3ca25636b5c56f`  
		Last Modified: Thu, 13 Jan 2022 16:11:43 GMT  
		Size: 61.0 MB (61010271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f4609300d658bf52b006741f5590abdf93d8d575e0ddf04ce5be28e82b50a4`  
		Last Modified: Thu, 13 Jan 2022 16:11:58 GMT  
		Size: 188.6 MB (188638449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:784cf3007996898653e12b85f6cf71597349b95377a60e1c57d40aaf682ddc3e`  
		Last Modified: Thu, 13 Jan 2022 16:11:32 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e291dafdd6a7112a1b18f88f42cbef2225094f58f18d2f364d0d34006b69e1`  
		Last Modified: Thu, 13 Jan 2022 16:11:30 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c90f666fc9fbd62181b8b51f391386e0a1a137451605b6f0a105171abe51380`  
		Last Modified: Thu, 13 Jan 2022 16:11:29 GMT  
		Size: 2.3 KB (2264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8abc3a9f73c2948571140a610a8c9f79b87c33bcbfdf320cd0f6e5d9fbe944`  
		Last Modified: Thu, 13 Jan 2022 16:11:29 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73634fb3f49af52529a1b025a3cebf50531fdbcbdb3876b7b00908dfe9dc0a85`  
		Last Modified: Thu, 13 Jan 2022 16:11:29 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kibana:7.17.3`

```console
$ docker pull kibana@sha256:2b8f01ffcf3c101406df1a146b98a021448eab14545179e7b145e66eabecf827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kibana:7.17.3` - linux; amd64

```console
$ docker pull kibana@sha256:2bea450207ac0574ea7b3cc4318c260100ed7722043c9e05cf857a2ff6e56050
```

-	Docker Version: 20.10.14
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.9 MB (324937357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4897f4b8b6ee94dc47ac4dc1274419806d370ea5351204caacc711fd24843b18`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Tue, 19 Apr 2022 09:09:34 GMT
EXPOSE 5601
# Tue, 19 Apr 2022 09:09:52 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code)
# Tue, 19 Apr 2022 09:09:53 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini
# Tue, 19 Apr 2022 09:09:53 GMT
RUN mkdir /usr/share/fonts/local
# Tue, 19 Apr 2022 09:09:54 GMT
RUN curl -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc
# Tue, 19 Apr 2022 09:09:55 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c -
# Tue, 19 Apr 2022 09:09:56 GMT
RUN fc-cache -v
# Tue, 19 Apr 2022 09:10:18 GMT
COPY --chown=1000:0dir:7e38b46db342337f732630ffefe1e08787c4a0d81898f5d9b6ea4631e27926f2 in /usr/share/kibana 
# Tue, 19 Apr 2022 09:10:26 GMT
WORKDIR /usr/share/kibana
# Tue, 19 Apr 2022 09:10:26 GMT
RUN ln -s /usr/share/kibana /opt/kibana
# Tue, 19 Apr 2022 09:10:26 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 19 Apr 2022 09:10:26 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Apr 2022 09:10:27 GMT
COPY --chown=1000:0file:6db5413736a28ead04731f52a5ef1acaa8f3ca1c1d2eaf6bb2b80d8f232794a2 in /usr/share/kibana/config/kibana.yml 
# Tue, 19 Apr 2022 09:10:27 GMT
COPY file:64ce3ba9275bed6c9214b200cd3b7913d52068df7094bee2baccc5b713d391f7 in /usr/local/bin/ 
# Tue, 19 Apr 2022 09:10:28 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \;
# Tue, 19 Apr 2022 09:10:29 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} +
# Tue, 19 Apr 2022 09:10:30 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana
# Tue, 19 Apr 2022 09:10:30 GMT
LABEL org.label-schema.build-date=2022-04-19T08:22:01.788Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=dcd0a101ed880bb10a4dcf511b91fd611d8c805d org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.3 org.opencontainers.image.created=2022-04-19T08:22:01.788Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=dcd0a101ed880bb10a4dcf511b91fd611d8c805d org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.3
# Tue, 19 Apr 2022 09:10:30 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 19 Apr 2022 09:10:30 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 19 Apr 2022 09:10:30 GMT
USER kibana
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9440443b08eec92ff612b85f90f6a222d0f51f1638a616df0c5fd66fdfa09d21`  
		Last Modified: Thu, 21 Apr 2022 21:47:42 GMT  
		Size: 11.1 MB (11104556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03e97b0672be8f3883010e630253121cd69d6610e32275a17a3ee52845741a3`  
		Last Modified: Thu, 21 Apr 2022 21:47:40 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aee45d3a5070a0a89d68d564d536015f2fd51e4d15976ee7bcb55269c28935b`  
		Last Modified: Thu, 21 Apr 2022 21:47:38 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9cd1a53684f0b291e74c318294c37f556b4c29b1f577f9c49368186464d86a`  
		Last Modified: Thu, 21 Apr 2022 21:47:39 GMT  
		Size: 16.5 MB (16460475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c3a32db2527717d18fdaec8cc4626c056bfd4aa985fbe00ec4ad66ad6b2359`  
		Last Modified: Thu, 21 Apr 2022 21:47:38 GMT  
		Size: 5.3 KB (5275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b931a580503e92f559a067657b0e1e5aa2fd87a5e5149ec45c485c0b2c14e92`  
		Last Modified: Thu, 21 Apr 2022 21:48:09 GMT  
		Size: 268.6 MB (268594419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5b3379fce708dba1be025f32353fbaf36185302cf1cb4ffdafd2ebc40ddd91`  
		Last Modified: Thu, 21 Apr 2022 21:47:38 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a844e9e78246da9700954e79aed2446d778a64b2a50cfacc5b0c5fa687141c`  
		Last Modified: Thu, 21 Apr 2022 21:47:35 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5c92edaabe39726c4ec16c21c4e6c9790f054e8e8c2270f1a210ec0bca6420`  
		Last Modified: Thu, 21 Apr 2022 21:47:35 GMT  
		Size: 4.5 KB (4498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b5eef01620ff76f54606aa6baf4d03c44085cf5ec4f532db3d5c4bf75b17dd`  
		Last Modified: Thu, 21 Apr 2022 21:47:35 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80b734e506d28d51f8b6e515cef6a6eb5ab1ca537de9c5791a28e79621d793b`  
		Last Modified: Thu, 21 Apr 2022 21:47:35 GMT  
		Size: 189.4 KB (189380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df86baf43ead418a0f9d4c82ce16e9663493178c2c9f4ed14892f41874a41e4`  
		Last Modified: Thu, 21 Apr 2022 21:47:35 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kibana:8.1.3`

```console
$ docker pull kibana@sha256:731d6a0cf046e343ad8d0ee9066e93b6438cafdda7888831300ede0c20dcbba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kibana:8.1.3` - linux; amd64

```console
$ docker pull kibana@sha256:03d6cf92844f5541099c24ffdbf8830e38b64dc3b9c1db882415529fecb93e00
```

-	Docker Version: 20.10.14
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.8 MB (309830968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bccb01e35afbeafaaa394c38da540899e8dc19147bda5963b6826566c973575`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Tue, 19 Apr 2022 12:00:08 GMT
EXPOSE 5601
# Tue, 19 Apr 2022 12:00:27 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code)
# Tue, 19 Apr 2022 12:00:28 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini
# Tue, 19 Apr 2022 12:00:28 GMT
RUN mkdir /usr/share/fonts/local
# Tue, 19 Apr 2022 12:00:30 GMT
RUN curl -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc
# Tue, 19 Apr 2022 12:00:30 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c -
# Tue, 19 Apr 2022 12:00:31 GMT
RUN fc-cache -v
# Tue, 19 Apr 2022 12:00:57 GMT
COPY --chown=1000:0dir:32745a83d1336d210214cc5c7f9840539516d8a764d7e7cd388382358efa4e4e in /usr/share/kibana 
# Tue, 19 Apr 2022 12:01:02 GMT
WORKDIR /usr/share/kibana
# Tue, 19 Apr 2022 12:01:02 GMT
RUN ln -s /usr/share/kibana /opt/kibana
# Tue, 19 Apr 2022 12:01:02 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 19 Apr 2022 12:01:02 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Apr 2022 12:01:03 GMT
COPY --chown=1000:0file:6db5413736a28ead04731f52a5ef1acaa8f3ca1c1d2eaf6bb2b80d8f232794a2 in /usr/share/kibana/config/kibana.yml 
# Tue, 19 Apr 2022 12:01:03 GMT
COPY file:7c7c9d2b7fd3a7bac99ec2cc74e9f55d2255b807334a4eb61596a05358fbcde2 in /usr/local/bin/ 
# Tue, 19 Apr 2022 12:01:04 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \;
# Tue, 19 Apr 2022 12:01:05 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} +
# Tue, 19 Apr 2022 12:01:06 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana
# Tue, 19 Apr 2022 12:01:06 GMT
LABEL org.label-schema.build-date=2022-04-19T11:53:51.363Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=c44c8c44c82ed80d1ae3dd990291dcc85b7a27dc org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.1.3 org.opencontainers.image.created=2022-04-19T11:53:51.363Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=c44c8c44c82ed80d1ae3dd990291dcc85b7a27dc org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.1.3
# Tue, 19 Apr 2022 12:01:06 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 19 Apr 2022 12:01:06 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 19 Apr 2022 12:01:06 GMT
USER kibana
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c296003de0686f08926be7640e6ef731c75717cad98bf6297f85f991c28b1e92`  
		Last Modified: Wed, 20 Apr 2022 18:45:03 GMT  
		Size: 11.1 MB (11104533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2495a47da476776e7104dfb6ae209cff849aeb5c8a7c68ea5380c55869f7de`  
		Last Modified: Wed, 20 Apr 2022 18:45:00 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f02379158206636cadf735a0a2570fa56435cd60a4c1b4357cd44bc59a0caa`  
		Last Modified: Wed, 20 Apr 2022 18:44:57 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeb34a3722b0f33264ea0e347d7d6be919ca2ca305d0e824cd5d6475c0c574e2`  
		Last Modified: Wed, 20 Apr 2022 18:44:59 GMT  
		Size: 16.5 MB (16460479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e61552359d75d5a9d527f4017c3282033757a0f0bbfc37c3bb47e7b954ec28e`  
		Last Modified: Wed, 20 Apr 2022 18:44:56 GMT  
		Size: 5.3 KB (5285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bd0e46d81c67f0d4e327e3e8d0de6461d29c56e0bf6fa154ac9903a13d223c`  
		Last Modified: Wed, 20 Apr 2022 18:45:50 GMT  
		Size: 253.5 MB (253488288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c649ba17a08185693d0a175cd1cc80f16d5cf8001422a38bde5ef72392771cc`  
		Last Modified: Wed, 20 Apr 2022 18:44:56 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413e0b7bc38aaa93c90f7f53d6794823f668e6412665871efc0934b0d3ecb541`  
		Last Modified: Wed, 20 Apr 2022 18:44:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc74e964cb98e991c21e7adfe8e4c9a1a2e331a8ff44972b483aca2a891c96a2`  
		Last Modified: Wed, 20 Apr 2022 18:44:53 GMT  
		Size: 4.2 KB (4234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bdab366aeacdd96640e9870ad0179ebfcb969b1f2cce91e426c207b76698191`  
		Last Modified: Wed, 20 Apr 2022 18:44:53 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c562a95de348585c2747fdc70b79e18776cf4cfba56a655163077c2fdd01ac9a`  
		Last Modified: Wed, 20 Apr 2022 18:44:53 GMT  
		Size: 189.4 KB (189381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c3fd9f47eba97297351be02cce9b710d725b003a32dae889037574d2e5ff69`  
		Last Modified: Wed, 20 Apr 2022 18:44:53 GMT  
		Size: 1.8 KB (1827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
