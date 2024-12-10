## `openjdk:25-ea-1-jdk`

```console
$ docker pull openjdk@sha256:a1524532942ef87969c70e22150a3605ea1599082377522bd048750cac39a3d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `openjdk:25-ea-1-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:176782a307f7ce50697a5b92d9f5e6a0185c4121b606acbd266aa97e147a8311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.7 MB (310724176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec00b6a1c73624f0d39f7ed76e625491149b2fc6ac1d5b0ee7bcd0e1e0142b0b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 05:52:24 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 09 Dec 2024 05:52:24 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Mon, 09 Dec 2024 05:52:24 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 05:52:24 GMT
ENV LANG=C.UTF-8
# Mon, 09 Dec 2024 05:52:24 GMT
ENV JAVA_VERSION=25-ea+1
# Mon, 09 Dec 2024 05:52:24 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/1/GPL/openjdk-25-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='b2c1c3716a21ae204e31e0f37782552ffef0f6e0d9850ba16fb57cd0fa98d84c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/1/GPL/openjdk-25-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='76761c3ad2bebc865c5ed4ce08a7c5f89eb4f51d3f471d76f650e0556d79daa3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 09 Dec 2024 05:52:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e5b1df7e6678619152ca0b4b1694bb07a547b66ace8461d2532c57140d1e6f`  
		Last Modified: Mon, 09 Dec 2024 23:31:01 GMT  
		Size: 48.8 MB (48764981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60adf24fd38e139d4c6dbab4c7d0f0c61d7a47637e28a92ae590d45795ab2ac`  
		Last Modified: Mon, 09 Dec 2024 23:31:03 GMT  
		Size: 212.9 MB (212860493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-1-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:bf8c9c060a38838190d3cc5a3aca72dd32af551ed28cbe268e0062636121f544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4937365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e0ea8f37c2af40eda347ad105c6c925a501ad817847595c895de536f339e20c`

```dockerfile
```

-	Layers:
	-	`sha256:6718ba1288415d851be9ac25e9a3380f66b801b50684bf2c1cd5e3fd11057dd3`  
		Last Modified: Mon, 09 Dec 2024 23:31:00 GMT  
		Size: 4.9 MB (4917646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8881f02f01bae8409dc96589d160bf8cd66234b4cadd51420a8409c7dff6196a`  
		Last Modified: Mon, 09 Dec 2024 23:30:59 GMT  
		Size: 19.7 KB (19719 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-1-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4fff5bf9d1dabdec03c754125ccf62af4dc2827b0840ec65412d623805b79514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307668552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e912529b31c480a840a331d35346e0065e540537b34bde07dac0b2b8a28cab49`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 05:52:24 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 09 Dec 2024 05:52:24 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Mon, 09 Dec 2024 05:52:24 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 05:52:24 GMT
ENV LANG=C.UTF-8
# Mon, 09 Dec 2024 05:52:24 GMT
ENV JAVA_VERSION=25-ea+1
# Mon, 09 Dec 2024 05:52:24 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/1/GPL/openjdk-25-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='b2c1c3716a21ae204e31e0f37782552ffef0f6e0d9850ba16fb57cd0fa98d84c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/1/GPL/openjdk-25-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='76761c3ad2bebc865c5ed4ce08a7c5f89eb4f51d3f471d76f650e0556d79daa3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 09 Dec 2024 05:52:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50730d7cdebc9dd971fe547b229ac9b36632531d0634a0903681766460bf2cf8`  
		Last Modified: Tue, 10 Dec 2024 01:26:17 GMT  
		Size: 49.2 MB (49196487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54af664e35ef103baa3b3dcc87df83716be18f396018f395d54cf53c3c756382`  
		Last Modified: Tue, 10 Dec 2024 01:26:21 GMT  
		Size: 210.8 MB (210804673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-1-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:ff0786f629fd7b9a8df53223b231fb534c316e524ee9c6e023a9d6099ce0e236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4935411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21ba25706f93f05661b7b75a1d8dbf71c440a1b48a99041bfc92919d10ab456`

```dockerfile
```

-	Layers:
	-	`sha256:1829300b15a64072b21464e8c7d35bb51b9f318c8a427e8f0e8bd25324a6cef9`  
		Last Modified: Tue, 10 Dec 2024 01:26:16 GMT  
		Size: 4.9 MB (4915404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ab117944861d14ed57e92f877a50ac792999bb144d27979d7215802d3d62762`  
		Last Modified: Tue, 10 Dec 2024 01:26:15 GMT  
		Size: 20.0 KB (20007 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-1-jdk` - windows version 10.0.20348.2849; amd64

```console
$ docker pull openjdk@sha256:1a748c153e40408b6a98ac41158362e3eda044bf98804decce613cef9bb2a72a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2462141129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134a6f3207995540f1dca2c8fdd2ab20c55407379a98250ec4a87487b6a05fac`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Mon, 09 Dec 2024 23:30:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 09 Dec 2024 23:30:49 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 09 Dec 2024 23:30:49 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 09 Dec 2024 23:30:57 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 09 Dec 2024 23:30:57 GMT
ENV JAVA_VERSION=25-ea+1
# Mon, 09 Dec 2024 23:30:58 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/1/GPL/openjdk-25-ea+1_windows-x64_bin.zip
# Mon, 09 Dec 2024 23:30:58 GMT
ENV JAVA_SHA256=e613057ce9dd454d410ac2462a504dd7679eeec29d28c18c9d16c6d12f12f346
# Mon, 09 Dec 2024 23:31:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 09 Dec 2024 23:31:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f62744fe0bffce54ba5c69993794a493843c155d541e18b0d74f9365ff6f07`  
		Last Modified: Mon, 09 Dec 2024 23:31:34 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dec8c4be008b03b6877f47753901f70a486eb2b094f302794690be01bc06154`  
		Last Modified: Mon, 09 Dec 2024 23:31:34 GMT  
		Size: 363.4 KB (363444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a3c453de130ff99a3d6f4cf73bf82b0a7085b98beb3e48482f8817aed6fdf1`  
		Last Modified: Mon, 09 Dec 2024 23:31:34 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9384c35821d963b7ac1a73f732165922794ef59958ddafb3100ba91fc51ce89`  
		Last Modified: Mon, 09 Dec 2024 23:31:34 GMT  
		Size: 347.2 KB (347190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fafd07f0b873df552e6d036c1491e18167cdb70d61048e9cfba67a359a1e435d`  
		Last Modified: Mon, 09 Dec 2024 23:31:33 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5515e93df28f8f47408a0476e608aca15b9b52350b657b0edffaafe332133f22`  
		Last Modified: Mon, 09 Dec 2024 23:31:33 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea4197bd5a482eed83557bce5b488187d0214329960e1ccd914ff3b6a1b748a`  
		Last Modified: Mon, 09 Dec 2024 23:31:33 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113bcb9ec4332b2f117ae80b264a590be20614177d2b66c22f4ce4ed81c00581`  
		Last Modified: Mon, 09 Dec 2024 23:31:44 GMT  
		Size: 208.9 MB (208938413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b0c92d636855cdb04428662688d9eee149c1ce9d32c1b88427b546b233ff47`  
		Last Modified: Mon, 09 Dec 2024 23:31:33 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-1-jdk` - windows version 10.0.17763.6532; amd64

```console
$ docker pull openjdk@sha256:cecd75e09367bcc34c77eae00e02890eae5273f541a6ddf6b178ef8b974d3e4a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2220419857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:783468780688e94afa2f1a9ae718fb13c7e4b9edd955491e84beacb5c77ef05f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Mon, 09 Dec 2024 23:29:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 09 Dec 2024 23:31:30 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 09 Dec 2024 23:31:31 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 09 Dec 2024 23:31:41 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 09 Dec 2024 23:31:42 GMT
ENV JAVA_VERSION=25-ea+1
# Mon, 09 Dec 2024 23:31:43 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/1/GPL/openjdk-25-ea+1_windows-x64_bin.zip
# Mon, 09 Dec 2024 23:31:43 GMT
ENV JAVA_SHA256=e613057ce9dd454d410ac2462a504dd7679eeec29d28c18c9d16c6d12f12f346
# Mon, 09 Dec 2024 23:32:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 09 Dec 2024 23:32:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6fd3dfa20c1d65d0268634885e1faf52e6ba86925cd04767a5dc79d3af0777`  
		Last Modified: Mon, 09 Dec 2024 23:32:36 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5a2a5b466475e162ebc994d3e4ca0c223fc4eb0505b61f7492ffd17b22a55b`  
		Last Modified: Mon, 09 Dec 2024 23:32:36 GMT  
		Size: 493.5 KB (493481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5fc9291fb3e0bac7eb383f54a5b6e187421a8246239ee999bd35deac416e855`  
		Last Modified: Mon, 09 Dec 2024 23:32:36 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d4e432b4ac9849e7414b7eb7acbe9b3162618f4decaa49d0a9babe008f0f40`  
		Last Modified: Mon, 09 Dec 2024 23:32:36 GMT  
		Size: 337.4 KB (337383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1d15bffa3da761d4a7e8fc12a1ddb6efdd261c5a52eae000c9a9fb99f7bbee`  
		Last Modified: Mon, 09 Dec 2024 23:32:35 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c428588222e233ad3d18afa39e9ac45d429f82702a5c8dee415b2d3df28b08`  
		Last Modified: Mon, 09 Dec 2024 23:32:35 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940130d3bd5135d42d05418c978115e11f4c7fd8408ceba7302ec66e220960bf`  
		Last Modified: Mon, 09 Dec 2024 23:32:35 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9fca6b37d9e796d535c5032975bbe4cb25c7958c09b2a536cd0ee4c952fa16`  
		Last Modified: Mon, 09 Dec 2024 23:32:46 GMT  
		Size: 208.9 MB (208927455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91996e0f386cdeef116835bfd2973420be828ec1a11b9504ea1413cbf92b9bf0`  
		Last Modified: Mon, 09 Dec 2024 23:32:35 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
