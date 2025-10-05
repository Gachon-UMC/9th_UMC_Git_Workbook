##### 1주차 학습내용 #####
* 1. 개념 *
기본 뷰와 레이아웃 구성에 대한 개념을 잡았다.

* 2. 실습 *
//
//  TicketView.swift
//  MegaBox
//
//  Created by 원서우 on 9/16/25.
//

import Foundation
import SwiftUI

struct TicketView: View {
    var body: some View {
        ZStack {
            Image(.background)
            
            VStack {
                
                Spacer().frame(height: 111)
                
                mainTitleGroup
                
                Spacer().frame(height: 134)
                
                mainBottomGroup
            }
        }
        .padding()
    }
    
    private var mainTitleGroup: some View {
        VStack {
            Group {
                Text("마이펫의 이중생활2")
                    .font(.PretendardBold18)
                    .shadow(color: .black.opacity(0.25), radius: 2, x: 0, y: 4)
                Text("본인 + 동반 1인")
                    .font(.PretendardLight14)
                Text("30,100원")
                    .font(.PretendardBold24)
            }
            .foregroundStyle(Color.white)
        }
        .frame(height: 84)
    }
    
    private var mainBottomGroup: some View {
        Button(action: {
            print("Hello")
        }, label: {
            VStack {
                Image(systemName: "chevron.up")
                    .resizable()
                    .frame(width: 18, height: 12)
                    .foregroundStyle(Color.white)
                Text("예매하기")
                    .font(.PretendardSemiBold18)
                    .foregroundStyle(Color.white)
            }
            .frame(width: 63, height: 40)
        })
    }
}

#Preview {
    TicketView()
}


* 3. 과제 *
//
//  LoginView.swift
//  MegaBox
//
//  Created by 원서우 on 9/20/25.
//

import Foundation
import SwiftUI

struct LoginView: View {
    @State private var viewModel: LoginViewModel = LoginViewModel()
    @AppStorage("id") private var id: String = ""
    @AppStorage("pwd") private var pwd: String = ""
    
    var body: some View {
        ZStack {
            Color.white00.ignoresSafeArea()
            VStack {
                navigationbar
                idpwdbtn.padding(.bottom, 77)
                Loginbtn.padding(.bottom, 17)
                addacountbtn.padding(.bottom, 35)
                socialLoginbtn.padding(.bottom, 39)
                Image(.UMC)
                    .resizable()
                    .frame(width: 408, height: 266)
            }
            .padding(.horizontal)
        }
    }

    private var navigationbar: some View {
        VStack {
            Text("로그인")
                .font(.PretendardSemiBold24)
            Spacer()
        }
    }
    
    private var idpwdbtn: some View {
        VStack {
                TextField("아이디", text: $viewModel.id)
                    .font(.PretendardMedium16)
                    .foregroundStyle(Color.gray03)
            Spacer().frame(height: 4)
            Divider()
                .foregroundStyle(Color.gray02)
            
            Spacer().frame(height: 40)
            
                SecureField("패스워드", text: $viewModel.pwd)
                    .font(.PretendardMedium16)
                    .foregroundStyle(Color.gray03)
            Spacer().frame(height: 4)
            Divider()
                .foregroundStyle(Color.gray02)
        }
        .padding(.horizontal)
    }

    
    private var Loginbtn: some View {
        Button(action: {
            print("로그인 Click!")
            id = "\(viewModel.id)"
            pwd = "\(viewModel.pwd)"
        }) {
            HStack(alignment: .center) {
                Text("로그인")
                    .font(.PretendardBold18)
                    .frame(maxWidth: .infinity, minHeight: 54)
                    .foregroundStyle(Color.white)
                    .background(Color.purple03)
                    .cornerRadius(10)
            }
            .padding(.horizontal)
        }
    }
    
    private var addacountbtn: some View {
        Button(action: {
            print("회원가입 Click!")
        }) {
            Text("회원가입")
                .font(.PretendardMedium13)
                .foregroundStyle(Color.gray04)
        }
    }
    
    private var socialLoginbtn: some View {
        HStack(alignment: .center, spacing: 73) {
            Image(.loginBtnN)
            Image(.loginBtnK)
            Image(.loginBtnA)
        }
    }
}



#Preview("iPhone 16 Pro") {
    LoginView()
}
