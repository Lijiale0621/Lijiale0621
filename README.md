- 👋 Hi, I’m @Lijiale0621
- 👀 I’m interested in animation
- 🌱 I’m currently learning python
- 💞️ I’m looking to collaborate on everyone
- 📫 How to reach me lijiale0621@gmail.com
- 😄 Pronouns: she/her

<!---
Lijiale0621/Lijiale0621 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

bpmn-mermaid
graph LR
    subgraph Pool_1[组织管理流程 / Organisational Management Process]
        direction LR
        Lane_A[组织/部门]
        Lane_B[员工个体]

        %% 组织端流程
        A1(活动: 设定高绩效预期/大工作量) --> A2(活动: 持续施加工作要求);
        
        %% 员工端流程 - 压力开始
        A2 --> B1{事件: 员工持续工作过长时间};
        B1 --> B2(活动: 投入过多时间与精力);
        
        %% 压力与福祉路径
        B2 --> B3_G{网关: 压力累积/资源消耗?};
        B3_G -->|是| B4[事件: 触发职业倦怠/福祉受损];
        
        %% WLB冲突路径
        B4 --> B5[事件: 无法履行家庭/个人角色 (WFC)];
        
        %% 态度和满意度评估
        B5 --> B6_G{网关: 员工感知价值差距/契约违背?};
        
        B6_G -->|是 (低感知)| B7[事件: 评估工作缺乏回报/不公平];
        B7 --> B8[事件: 工作满意度急剧下降];
        
        %% 最终行为结果
        B8 --> B9(活动: 考虑离职/减少 OCB/消极行为);
        
        %% 资源和支持的分支 (避免满意度下降)
        B3_G -->|否 (资源充足)| B_X[事件: 工作要求被有效抵消/恢复];
        B_X --> B_Y[事件: 工作满意度维持或提高];
        
        B6_G -->|否 (高感知)| B_Y;
    end
