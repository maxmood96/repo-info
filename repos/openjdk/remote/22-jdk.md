## `openjdk:22-jdk`

```console
$ docker pull openjdk@sha256:565d995bfdc6b9fecc059ce172f5c2e597c8631b85d8addc31588e067fea0c67
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `openjdk:22-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:9f18c0ff81663cd12be5c4c4363d69da19fe52683f6f3f3c4272b6c90b4229da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269097900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93005b58dc2ac7b4c5195a1f46fe5e2a95ebf7a3d4d352f5f17dbdbc5aa02a0`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 07 Feb 2024 00:02:34 GMT
ADD file:ee9ade66919e02c9625e92c89cc2bde2568f070446ebcef5a45409031767cae2 in / 
# Wed, 07 Feb 2024 00:02:35 GMT
CMD ["/bin/bash"]
# Fri, 09 Feb 2024 19:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 09 Feb 2024 19:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 09 Feb 2024 19:48:12 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Feb 2024 19:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 09 Feb 2024 19:48:12 GMT
ENV JAVA_VERSION=22
# Fri, 09 Feb 2024 19:48:12 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/35/GPL/openjdk-22_linux-x64_bin.tar.gz'; 			downloadSha256='37b0e1d93e9b6478824c21753f2e8445c8caad885a2245f393b35658be1695b3'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/35/GPL/openjdk-22_linux-aarch64_bin.tar.gz'; 			downloadSha256='5bc8c3ea634bf3be8a275c789dabbaa3e68eb639ee920b6fbce1b2236082086d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 09 Feb 2024 19:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b8307a22608d5df5e6e46cb974e41cd9778a2521f94cbba7113f1bdcc8d10881`  
		Last Modified: Wed, 07 Feb 2024 00:04:12 GMT  
		Size: 51.3 MB (51327391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06013eaee161956a1c76abed2b359d338f1eedae57a9052729bde0526f31c01`  
		Last Modified: Mon, 12 Feb 2024 21:55:15 GMT  
		Size: 15.0 MB (15005782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20a786c0d635c5512e92683864c37f64272332ed7fb2a78d7337b8a1ad792c7`  
		Last Modified: Mon, 12 Feb 2024 21:55:18 GMT  
		Size: 202.8 MB (202764727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:4b697223aa9a6f30dd62b6be7af055d76bad16832c274753d44f353f0364984d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1931978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91102341c30dd707b9753a02c44edcd20354457cc1d4f2d66fd79799f1181002`

```dockerfile
```

-	Layers:
	-	`sha256:8371f7d6296cd240e0fb8236f971a6177c5c653e8cb7a7f779bef13a13a26ea3`  
		Last Modified: Mon, 12 Feb 2024 21:55:15 GMT  
		Size: 1.9 MB (1913954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbb879c156ee2bffe7eec397724f55c9dff1e5af6721c1f59d1568fcd4632685`  
		Last Modified: Mon, 12 Feb 2024 21:55:15 GMT  
		Size: 18.0 KB (18024 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:87d7f26a9a13430322797e1ddf787f5593ab8dc36d28e7c6dcc0551647000fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266586876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2a04ab388d407ab1ffdaf4ad755bf799056ba06844d69f85a10c6a3e04abdf`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 06 Feb 2024 22:04:58 GMT
ADD file:cd2f7e73ea216c58af8e2422d8e7fdd8cdc79f510d74cf24416e3a3f4929f8c2 in / 
# Tue, 06 Feb 2024 22:04:58 GMT
CMD ["/bin/bash"]
# Fri, 09 Feb 2024 19:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 09 Feb 2024 19:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 09 Feb 2024 19:48:12 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Feb 2024 19:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 09 Feb 2024 19:48:12 GMT
ENV JAVA_VERSION=22
# Fri, 09 Feb 2024 19:48:12 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/35/GPL/openjdk-22_linux-x64_bin.tar.gz'; 			downloadSha256='37b0e1d93e9b6478824c21753f2e8445c8caad885a2245f393b35658be1695b3'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/35/GPL/openjdk-22_linux-aarch64_bin.tar.gz'; 			downloadSha256='5bc8c3ea634bf3be8a275c789dabbaa3e68eb639ee920b6fbce1b2236082086d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 09 Feb 2024 19:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0647c03756d6c2108bc331960a270dba455e910d0f076e51ad650f96b8c54db9`  
		Last Modified: Tue, 06 Feb 2024 22:06:18 GMT  
		Size: 50.1 MB (50077424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04d3eef9c8a6237c8b46c9794501777a8ce3c58a2e3a645da53db98f8e028aa`  
		Last Modified: Tue, 06 Feb 2024 23:32:40 GMT  
		Size: 15.7 MB (15691300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76722c4edacd1fd68218c0562411b0ac7c222a22901c1880f4a489b1351fd0c2`  
		Last Modified: Tue, 13 Feb 2024 00:30:03 GMT  
		Size: 200.8 MB (200818152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:94b0ab1977c65de9b8648d11a20d9910c1d0f0e83efd06e5b97e4f84e93a2174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1931360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18df53ba898ee7a49af885505e0dec9a86aa676dedbdb56cc26b3dad3ce6a983`

```dockerfile
```

-	Layers:
	-	`sha256:71ec43d9e73b8601b8ffc6772d36955c21d08b7f602785331589223c77b6f82c`  
		Last Modified: Tue, 13 Feb 2024 00:29:58 GMT  
		Size: 1.9 MB (1913476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c96bf1d42a1bba24cebd4942cf587b9ec746a227f2ada3c873b56b0a93e2cda`  
		Last Modified: Tue, 13 Feb 2024 00:29:58 GMT  
		Size: 17.9 KB (17884 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-jdk` - windows version 10.0.20348.2227; amd64

```console
$ docker pull openjdk@sha256:8c083eeb23c7f10bea82dc294756cc305f60d53fa4394f8eb5178ddc9f1b9799
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2098780895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2340c26a29a33565627c822072d49a83b6f74ace5b1aa83f65cd5e4860b68c00`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Mon, 12 Feb 2024 21:54:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 12 Feb 2024 21:55:27 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 12 Feb 2024 21:55:28 GMT
ENV JAVA_HOME=C:\openjdk-22
# Mon, 12 Feb 2024 21:55:34 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 12 Feb 2024 21:55:34 GMT
ENV JAVA_VERSION=22
# Mon, 12 Feb 2024 21:55:35 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/35/GPL/openjdk-22_windows-x64_bin.zip
# Mon, 12 Feb 2024 21:55:36 GMT
ENV JAVA_SHA256=66546cc473f6f4ebb8161a8664afc6e04fa80cdf5c93a33e07f57eb1c27d6682
# Mon, 12 Feb 2024 21:56:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 12 Feb 2024 21:56:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3c92a169aff0fbe39f90be6e7bf78ad308fc207e4d5d00c6da8a89c6cee856`  
		Last Modified: Mon, 12 Feb 2024 21:56:12 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28bcd82b19e407e4a06b721810648213702f181084f9dad729b6673ebce8948`  
		Last Modified: Mon, 12 Feb 2024 21:56:12 GMT  
		Size: 487.7 KB (487671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbc6176c976ab9b643ead029cae643ada7fe83381046a0fbdbdb576ffd7e214`  
		Last Modified: Mon, 12 Feb 2024 21:56:11 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2974f7a2d571d414b99ca2d5f42722a049ac381372bfb8913829a11ce0dc5be`  
		Last Modified: Mon, 12 Feb 2024 21:56:12 GMT  
		Size: 338.9 KB (338860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99179ed1c951dc67a51b5114d5846f714d429f3445d898d5f81fa0534ab305bc`  
		Last Modified: Mon, 12 Feb 2024 21:56:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd6afb562ca2ecac5098878175089b002626d611fbab7050aa359f44d68a1232`  
		Last Modified: Mon, 12 Feb 2024 21:56:09 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb89efe3125560b0cd05fc8448bff3e41f87419af1b6bf9374aff880e94ea15`  
		Last Modified: Mon, 12 Feb 2024 21:56:09 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5478e1c9d936842287b71b5a54aa792ab3bb6fdf9c103879d0b47d6775bd6808`  
		Last Modified: Mon, 12 Feb 2024 21:56:20 GMT  
		Size: 197.7 MB (197733861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff55eb7b5cfa9dffd040895617be281a9105acddfcbc05eabc937c560b34ae2`  
		Last Modified: Mon, 12 Feb 2024 21:56:09 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-jdk` - windows version 10.0.17763.5329; amd64

```console
$ docker pull openjdk@sha256:fa0529de5556aa54f6dcbc6119d7144210c7e0f6b1a838aff9e28a8c6af96ab4
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2268324672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ffa96e04e9c0f98b16fb9307684d54cbe79286e063e2eae2e83acb01d2902c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Mon, 12 Feb 2024 21:54:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 12 Feb 2024 21:56:23 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 12 Feb 2024 21:56:23 GMT
ENV JAVA_HOME=C:\openjdk-22
# Mon, 12 Feb 2024 21:56:45 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 12 Feb 2024 21:56:46 GMT
ENV JAVA_VERSION=22
# Mon, 12 Feb 2024 21:56:46 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/35/GPL/openjdk-22_windows-x64_bin.zip
# Mon, 12 Feb 2024 21:56:47 GMT
ENV JAVA_SHA256=66546cc473f6f4ebb8161a8664afc6e04fa80cdf5c93a33e07f57eb1c27d6682
# Mon, 12 Feb 2024 21:57:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 12 Feb 2024 21:57:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66115862fdd12f1a4dc49354594a1a70d7ed118f0318c9bf7aaefeb832be00e8`  
		Last Modified: Mon, 12 Feb 2024 21:57:41 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabb396834b1f0758ec27d373b8a990adcdf09df0398610fd5e67b5938dbe8aa`  
		Last Modified: Mon, 12 Feb 2024 21:57:41 GMT  
		Size: 501.0 KB (500959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e449a079a6c7d6ec2563ee79bfedb15350b9774ddd58ab86ff50ba7c96d99a`  
		Last Modified: Mon, 12 Feb 2024 21:57:40 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e5ba5c85458c237c914c7cdc97982e75c7cff5abf3e677db1d55d6954fbce3`  
		Last Modified: Mon, 12 Feb 2024 21:57:41 GMT  
		Size: 348.2 KB (348221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866eee46cb0149d9127219fb2bdeb4756635fe31f330e8c3acd9d9ed9b11b9ec`  
		Last Modified: Mon, 12 Feb 2024 21:57:39 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ced1b7c144b3c30be8ca11d7d73b740557cfea101e5e58c4bec0a0449aab8f2`  
		Last Modified: Mon, 12 Feb 2024 21:57:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebfb199ca6296ceb433f5ee203ed0cd7c6c606eaaa6383e273f1cd20cb369bc`  
		Last Modified: Mon, 12 Feb 2024 21:57:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f390dc854610786b5069140540139b43e9ceb203196b2fc63fd3847c3830390`  
		Last Modified: Mon, 12 Feb 2024 21:57:49 GMT  
		Size: 197.7 MB (197745217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a06cf25d94dc6ed36090b74f4d20a91ff42decd23fb283d367bda6259b78bf`  
		Last Modified: Mon, 12 Feb 2024 21:57:39 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
