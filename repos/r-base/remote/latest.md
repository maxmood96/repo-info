## `r-base:latest`

```console
$ docker pull r-base@sha256:0b0607e2c36da0daebdf14baf075cbd6f22faedde94842a2495e409c92ae5faa
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

### `r-base:latest` - linux; amd64

```console
$ docker pull r-base@sha256:f0aa86e849000b6874e3111cd038b5c080f2933ad8f44feee4c056fa686caffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.8 MB (355816491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41138379afa1e9e804dcacdcdfcd06f5f173cb7f50f059905ef63159c97e48ed`
-	Default Command: `["R"]`

```dockerfile
# Sun, 16 Jun 2024 13:02:54 GMT
ADD file:c90c835a37f0040007d62990bb1a7701bf8fac5f7be2a95c4f7a4c904831114d in / 
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["bash"]
# Sun, 16 Jun 2024 13:02:54 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Sun, 16 Jun 2024 13:02:54 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LC_ALL=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LANG=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV R_BASE_VERSION=4.4.1
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:276a3574c9ee1c4e17bd0ae7c30a212b1753e64ed85ab3e2e18b0cb5c66114cb`  
		Last Modified: Tue, 13 Aug 2024 00:26:09 GMT  
		Size: 52.8 MB (52841190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7e3bcf11826e1c58f3f53681a75a9468ffb5390fa996cf28f29625e30b5bae`  
		Last Modified: Tue, 13 Aug 2024 01:14:07 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12e3b0df693332bb84c9a2d3b2c9f705d348aa13cccddcc253d84d8cb3b6bfa`  
		Last Modified: Tue, 13 Aug 2024 01:14:09 GMT  
		Size: 23.1 MB (23113147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03de7709f4a5a122b9c31d57a8202e7a621c0fe4efb65d546dbdb147c22777df`  
		Last Modified: Tue, 13 Aug 2024 01:14:07 GMT  
		Size: 866.7 KB (866718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bba00ee45f6522db319e4a0ca8c26790da461dc701c06e2816d91ad0937414e`  
		Last Modified: Tue, 13 Aug 2024 01:14:08 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1f9566172e98f2c124dc0d527eb84a49f131779581b97ad2024419ef159d88`  
		Last Modified: Tue, 13 Aug 2024 01:14:18 GMT  
		Size: 279.0 MB (278991777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:b9a203f4f9fd1ddbd1f37c051ebc8c011767bf9027c93e3df7cd982a512fa4ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12444396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922a708b6a6e7278824882c85cc768968b09aa595f15d3c2ac870e675ef3df06`

```dockerfile
```

-	Layers:
	-	`sha256:a55033b6796433af8d73efdb1172ac558b51af065accbf0b5d5b569114029061`  
		Last Modified: Tue, 13 Aug 2024 01:14:07 GMT  
		Size: 12.4 MB (12426467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4276081d076686ed7575a7491136064c8eebc2b84f585dc0a3b056840177818`  
		Last Modified: Tue, 13 Aug 2024 01:14:07 GMT  
		Size: 17.9 KB (17929 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; arm64 variant v8

```console
$ docker pull r-base@sha256:8fd498d4d96d32641c7369cecb7950043e5d863ba34ac87bf8cf18ab1c9b8a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.1 MB (341108151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f740335d5e86f4081b9558387c16cffd70c210d431c492e9d990612ea9ad6d0`
-	Default Command: `["R"]`

```dockerfile
# Sun, 16 Jun 2024 13:02:54 GMT
ADD file:8e46df4c5628fc2d0e9a0a8340d8fa4ae995b7f8eaea4a37d8c2340483d7f6ba in / 
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["bash"]
# Sun, 16 Jun 2024 13:02:54 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Sun, 16 Jun 2024 13:02:54 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LC_ALL=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LANG=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV R_BASE_VERSION=4.4.1
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:516e6d7b27c596c99ccee734286b90644fb195a47b2b25bde8302e9b90e7bb8a`  
		Last Modified: Tue, 13 Aug 2024 00:45:09 GMT  
		Size: 53.2 MB (53152442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bd469eba9ebd99a303eae74bf75785621baf8f869f0e3b378fc8fba8bb297b`  
		Last Modified: Tue, 13 Aug 2024 11:17:51 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6c2bea2eee398b421e5a152466c504ae7144dcb2c21601fc759e24efa454c0`  
		Last Modified: Tue, 13 Aug 2024 11:17:52 GMT  
		Size: 23.1 MB (23101723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8361d405803ffb19da2b070ee6408b0a92d1238da908772c1f71026d697baad`  
		Last Modified: Tue, 13 Aug 2024 11:17:51 GMT  
		Size: 866.7 KB (866718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80867bb39b8291d0649d9f070672ade295d2eddd6aecfd53c2c16e1941fb976d`  
		Last Modified: Tue, 13 Aug 2024 11:17:52 GMT  
		Size: 348.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bb240c078d6a9ed376e6f1f9347becf129557b10988578d1a1c91d4c386534`  
		Last Modified: Tue, 13 Aug 2024 11:17:58 GMT  
		Size: 264.0 MB (263983609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:605d93ebb7355f2104e7cfb04a295e4acde9eac0d5cdeb0b62ee98ae8eb56b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 MB (12542130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa15cd9a2278859e1287188235c4d0bc9976becb91595db48ab407b48ffdeab`

```dockerfile
```

-	Layers:
	-	`sha256:8e6b20321edc1b9cd100de5b05425a515f705bb41e85e94abb57e5cee8b0d745`  
		Last Modified: Tue, 13 Aug 2024 11:17:51 GMT  
		Size: 12.5 MB (12523922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92c8cc8879b0ebceb116a0d91289ea69a4e245131c4dac765b642e0e170f63fd`  
		Last Modified: Tue, 13 Aug 2024 11:17:51 GMT  
		Size: 18.2 KB (18208 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; ppc64le

```console
$ docker pull r-base@sha256:94bcfb63fbf32ee089b4ed770ded0f523b94ee8da615e5577f2de92f9249c9f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.6 MB (350624129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86096d898f7522ff09dd87f0291b5b8e528b4918fa85c9c10644de69695c1b53`
-	Default Command: `["R"]`

```dockerfile
# Sun, 16 Jun 2024 13:02:54 GMT
ADD file:12b03032064b0d5c80915c492086c246ce1d59ac440f1c69120dbbd189616533 in / 
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["bash"]
# Sun, 16 Jun 2024 13:02:54 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Sun, 16 Jun 2024 13:02:54 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LC_ALL=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LANG=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV R_BASE_VERSION=4.4.1
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:f628e11a36e335721280197a03583f0306cbf039619a6c06323192058009cb53`  
		Last Modified: Tue, 13 Aug 2024 00:29:34 GMT  
		Size: 56.8 MB (56775585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1dddc911541c031402aa53ffc7ba060608dd41593ff656474ac3e53f7f32479`  
		Last Modified: Tue, 13 Aug 2024 12:05:57 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3145093b8dbca2fbb914521c85e83eed486b06ff81edf7492fa8af50b6f0b549`  
		Last Modified: Tue, 13 Aug 2024 12:05:58 GMT  
		Size: 23.3 MB (23338626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd06846daa76734e58cd5ad42f8e28bfb09d0ae6a80252d25ee76c96f608fb61`  
		Last Modified: Tue, 13 Aug 2024 12:05:58 GMT  
		Size: 866.7 KB (866714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9227d8cbcd67ab83dbff0de5733349e1023cc18c64025a77948bad2e4d381be4`  
		Last Modified: Tue, 13 Aug 2024 12:05:58 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df64ef2ed6e6f163f4482fd1de97f702a1eee773950fbec38b6b04ea69ab844a`  
		Last Modified: Tue, 13 Aug 2024 12:06:05 GMT  
		Size: 269.6 MB (269639545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:b8a4a5d8e772c8a8123919cd83497b3a0e5392d4e614523e3119c63600247d8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12438449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ff26269f2648f2f3ebba9052fc454b96cd306f95f126a4736ef8057b7e906a`

```dockerfile
```

-	Layers:
	-	`sha256:075da8489ab937070007f90bb72f7871ff83a5e763d01ca81442756619fa345b`  
		Last Modified: Tue, 13 Aug 2024 12:05:58 GMT  
		Size: 12.4 MB (12420486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6182217d6996469c91e3fee5508b299d55ccc1b6b0c5f8f6f6d7534e94a86e5`  
		Last Modified: Tue, 13 Aug 2024 12:05:57 GMT  
		Size: 18.0 KB (17963 bytes)  
		MIME: application/vnd.in-toto+json

### `r-base:latest` - linux; s390x

```console
$ docker pull r-base@sha256:43d4ff564eb5a0395f169915041763c6c1eaf006e54d43fa4a7fbb3c76a06b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.9 MB (322899245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6908a89cdc8b95b1101a62bf3a2e9fd526eb07b295dcc28c40e8afee486216bc`
-	Default Command: `["R"]`

```dockerfile
# Sun, 16 Jun 2024 13:02:54 GMT
ADD file:ed752b0badb744224b241435cc89ae12d907a42dd7d2f82dd6104492ce4dac7c in / 
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["bash"]
# Sun, 16 Jun 2024 13:02:54 GMT
LABEL org.opencontainers.image.licenses=GPL-2.0-or-later org.opencontainers.image.source=https://github.com/rocker-org/rocker org.opencontainers.image.vendor=Rocker Project org.opencontainers.image.authors=Dirk Eddelbuettel <edd@debian.org>
# Sun, 16 Jun 2024 13:02:54 GMT
RUN useradd -s /bin/bash -m docker 	&& usermod -a -G staff docker # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8 # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LC_ALL=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
ENV LANG=en_US.UTF-8
# Sun, 16 Jun 2024 13:02:54 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list         && echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default         && echo 'APT::Install-Recommends "false";' > /etc/apt/apt.conf.d/90local-no-recommends # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
ENV R_BASE_VERSION=4.4.1
# Sun, 16 Jun 2024 13:02:54 GMT
RUN apt-get update         && apt-get install -y -t unstable --no-install-recommends                 libopenblas0-pthread 		littler                 r-cran-docopt                 r-cran-littler 		r-base=${R_BASE_VERSION}-* 		r-base-dev=${R_BASE_VERSION}-*                 r-base-core=${R_BASE_VERSION}-* 		r-recommended=${R_BASE_VERSION}-* 	&& chown root:staff "/usr/local/lib/R/site-library" 	&& chmod g+ws "/usr/local/lib/R/site-library" 	&& ln -s /usr/lib/R/site-library/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/lib/R/site-library/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installBioc.r /usr/local/bin/installBioc.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installDeps.r /usr/local/bin/installDeps.r 	&& ln -s /usr/lib/R/site-library/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/lib/R/site-library/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Jun 2024 13:02:54 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:fbb046efc9e91cdd2b169c0d71ad77aca5166c293df778872751338e08dfc6ab`  
		Last Modified: Tue, 13 Aug 2024 00:49:17 GMT  
		Size: 52.5 MB (52480916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d028461038616bd29878a538fa3fe6842a19e33395d213844bbad5504bef25e`  
		Last Modified: Tue, 13 Aug 2024 09:36:23 GMT  
		Size: 3.3 KB (3311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29527f3dfbbc65192c914c97f7d71018593daffdcf9c95bd560750cd4179b903`  
		Last Modified: Tue, 13 Aug 2024 09:36:27 GMT  
		Size: 23.2 MB (23223343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8adeedec6dd82d5b06ae2fe1cbcae4fdbec8f972e61e04f451f39da6e787b3cc`  
		Last Modified: Tue, 13 Aug 2024 09:36:23 GMT  
		Size: 923.5 KB (923488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387e713db28241f883199a27189bb602f5239bd1b08f82c9619f85601efbd975`  
		Last Modified: Tue, 13 Aug 2024 09:36:24 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db1a2c20016803afc7da0d9565361cc7726e806fe0b390b9ced1250516da2a5`  
		Last Modified: Tue, 13 Aug 2024 09:36:29 GMT  
		Size: 246.3 MB (246267837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `r-base:latest` - unknown; unknown

```console
$ docker pull r-base@sha256:9ce4db0ac31b89f9bc87b51504f2002fbc93c9d7d1a7a15b603220b36e8b64d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12245034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ce93f4da43ed8977e68de2c49c7f682ea5595d15f1b1591b4248b3a1befa06f`

```dockerfile
```

-	Layers:
	-	`sha256:5778d0637dce42ea0971031b7a0c228d49eb4958d8d3e9e5aa20437cb40619aa`  
		Last Modified: Tue, 13 Aug 2024 09:36:23 GMT  
		Size: 12.2 MB (12227105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc5a804742f07f18b8005120364346db6b3a9f76dc8e315bb6a99f82ead13c57`  
		Last Modified: Tue, 13 Aug 2024 09:36:23 GMT  
		Size: 17.9 KB (17929 bytes)  
		MIME: application/vnd.in-toto+json
